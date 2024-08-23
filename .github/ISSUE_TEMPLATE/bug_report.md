name: Bug report
about: Create a report to help us improve
title: ''
labels: bug
assignees: Maxlego08
body:
  - type: markdown
    attributes:
      value: |
        ## READ AND FOLLOW THE DESCRIPTIONS OF THIS ISSUE TEMPLATE!
        Not doing so may result in your issue being closed without warning. Take your time and properly fill out everything as requested.
        We advise you to put a maximum of image and video to better understand your problem.
  - type: checkboxes
    id: searched
    attributes:
      label: Terms
      options:
        - label: "I'm using the very latest version of zEssentials and its dependencies (zMenu and PlaceholdersAPI)."
          required: true
        - label: "I am sure this is a bug and it is not caused by a misconfiguration or by another plugin."
          required: true
        - label: "I've looked for already existing issues on the [Issue Tracker](https://github.com/Maxlego08/zEssentials/issues) and haven't found any."
          required: true
        - label: "I already searched on the [plugin wiki](https://zessentials.groupez.dev/) to know if a solution is already known."
          required: true
        - label: "I already searched on the [discord](https://discord.groupez.dev/) to check if anyone already has a solution for this."
          required: true
        - label: "I tested this with just zEssentials and its dependencies and with a vanilla client of the same version as the Server."
          required: true
        - label: "I enabled the debug mode in config.yml and sql debug"
          required: true    
  - type: input
    id: discord_tag
    attributes:
      label: Discord Username (optional)
      description: So I can contact you quickly.
      placeholder: ex. mydiscord123
    validations:
      required: false
  - type: dropdown
   id: server_version
   attributes:
     label: Server Version
     options:
       - 1.21.1
       - 1.21
       - 1.20.6
       - 1.20.4
   validations:
     required: true
  - type: textarea
    id: server_software
    attributes:
      label: Server Software
      description: "run `/version` command and paste it here"
      placeholder: |
        Run `/version` command and paste it here
        
        Example:
        This server is running Paper version git-Paper-130 (MC: 1.21) (Implementing API version 1.21-R0.1-SNAPSHOT)"
    validations:
      required: true
  - type: textarea
    id: plugin_version
    attributes:
      label: zEssentials Version
      description: "Execute `/version zEssentials` and paste the output here."
      placeholder: |
        Run `/version zEssentials` in your server and paste the output here.
        DO NOT PUT "LATEST". DOING SO WILL GET YOUR ISSUE CLOSED!
        
        Example:
        zEssentials version 1.0.0.6
    validations:
      required: true
  - type: textarea
    id: zmenu_version
    attributes:
      label: zMenu Version
      description: "Execute `/version zMenu` and paste the output here."
      placeholder: |
        Run `/version zMenu` in your server and paste the output here.
        DO NOT PUT "LATEST". DOING SO WILL GET YOUR ISSUE CLOSED!
        
        Example:
        zMenu version 1.0.3.4
    validations:
      required: true
  - type: textarea
    id: what-happened
    attributes:
      label: What happened?
      description: A clear and concise description of what the bug is.
      placeholder: "Example: The command /gamemode creative does not put me in creative"
    validations:
      required: true
  - type: textarea
    id: steps
    attributes:
      label: Steps to reproduce the issue
      description: Describe how to reproduce the issue step by step
      placeholder: |
        1. Go to '...'
        2. Click on '....'
        3. Scroll down to '....'
        4. See error
    validations:
      required: true
  - type: input
    id: full_server_log
    attributes:
      label: Full Server Log
      description: |-
        Upload your latest.log file to [mclo.gs](https://mclo.gs) and share the generated URL here.
        Sensitive info such as IPs will automatically be censored for your privacy.
      placeholder: "https://mclo.gs/..."  
    validations:
      required: true
  - type: textarea
    id: errors
    attributes:
      label: Error (optional)
      description: "Paste any errors you have here. Text pasted here will be formatted as code. This allows us to see the problem directly without having to search in the logs."
      render: shell
      placeholder: |
        [16:59:59 WARN]: java.sql.SQLException: Failed to execute upsert: No operations allowed after statement closed.
[16:59:59 WARN]:        at zEssentials-1.0.0.4.jar//fr.maxlego08.essentials.libs.sarah.requests.UpsertRequest.execute(UpsertRequest.java:82)
[16:59:59 WARN]:        at zEssentials-1.0.0.4.jar//fr.maxlego08.essentials.libs.sarah.SchemaBuilder.execute(SchemaBuilder.java:605)
[16:59:59 WARN]:        at zEssentials-1.0.0.4.jar//fr.maxlego08.essentials.storage.database.Repository.upsert(Repository.java:38)
[16:59:59 WARN]:        at zEssentials-1.0.0.4.jar//fr.maxlego08.essentials.storage.database.repositeries.UserEconomyRepository.upsert(UserEconomyRepository.java:21)
[16:59:59 WARN]:        at zEssentials-1.0.0.4.jar//fr.maxlego08.essentials.storage.storages.SqlStorage.lambda$updateEconomy$4(SqlStorage.java:215)
[16:59:59 WARN]:        at zEssentials-1.0.0.4.jar//fr.maxlego08.essentials.zutils.utils.StorageHelper.lambda$async$0(StorageHelper.java:31)
[16:59:59 WARN]:        at zEssentials-1.0.0.4.jar//fr.maxlego08.essentials.libs.folialib.impl.SpigotImplementation.lambda$runAsync$1(SpigotImplementation.java:51)
[16:59:59 WARN]:        at org.bukkit.craftbukkit.scheduler.CraftTask.run(CraftTask.java:88)
[16:59:59 WARN]:        at org.bukkit.craftbukkit.scheduler.CraftAsyncTask.run(CraftAsyncTask.java:57)
[16:59:59 WARN]:        at com.destroystokyo.paper.ServerSchedulerReportingWrapper.run(ServerSchedulerReportingWrapper.java:22)
[16:59:59 WARN]:        at java.base/java.util.concurrent.ThreadPoolExecutor.runWorker(ThreadPoolExecutor.java:1144)
[16:59:59 WARN]:        at java.base/java.util.concurrent.ThreadPoolExecutor$Worker.run(ThreadPoolExecutor.java:642)
[16:59:59 WARN]:        at java.base/java.lang.Thread.run(Thread.java:1583)
[16:59:59 WARN]: Caused by: java.sql.SQLException: No operations allowed after statement closed.
[16:59:59 WARN]:        at com.mysql.cj.jdbc.exceptions.SQLError.createSQLException(SQLError.java:121)
[16:59:59 WARN]:        at com.mysql.cj.jdbc.exceptions.SQLError.createSQLException(SQLError.java:89)
[16:59:59 WARN]:        at com.mysql.cj.jdbc.exceptions.SQLError.createSQLException(SQLError.java:81)
[16:59:59 WARN]:        at com.mysql.cj.jdbc.exceptions.SQLError.createSQLException(SQLError.java:55)
[16:59:59 WARN]:        at com.mysql.cj.jdbc.exceptions.SQLError.createSQLException(SQLError.java:65)
[16:59:59 WARN]:        at com.mysql.cj.jdbc.exceptions.SQLExceptionsMapping.translateException(SQLExceptionsMapping.java:73)
[16:59:59 WARN]:        at com.mysql.cj.jdbc.ClientPreparedStatement.checkBounds(ClientPreparedStatement.java:1404)
[16:59:59 WARN]:        at com.mysql.cj.jdbc.ClientPreparedStatement.getCoreParameterIndex(ClientPreparedStatement.java:1408)
[16:59:59 WARN]:        at com.mysql.cj.jdbc.ClientPreparedStatement.setObject(ClientPreparedStatement.java:1682)
[16:59:59 WARN]:        at zEssentials-1.0.0.4.jar//fr.maxlego08.essentials.libs.sarah.requests.UpsertRequest.execute(UpsertRequest.java:76)
[16:59:59 WARN]:        ... 12 more
[16:59:59 WARN]: Caused by: com.mysql.cj.exceptions.StatementIsClosedException: No operations allowed after statement closed.
[16:59:59 WARN]:        at java.base/jdk.internal.reflect.DirectConstructorHandleAccessor.newInstance(DirectConstructorHandleAccessor.java:62)
[16:59:59 WARN]:        at java.base/java.lang.reflect.Constructor.newInstanceWithCaller(Constructor.java:502)
[16:59:59 WARN]:        at java.base/java.lang.reflect.Constructor.newInstance(Constructor.java:486)
[16:59:59 WARN]:        at com.mysql.cj.exceptions.ExceptionFactory.createException(ExceptionFactory.java:52)
[16:59:59 WARN]:        at com.mysql.cj.exceptions.ExceptionFactory.createException(ExceptionFactory.java:76)
[16:59:59 WARN]:        at com.mysql.cj.jdbc.StatementImpl.checkClosed(StatementImpl.java:352)
[16:59:59 WARN]:        at com.mysql.cj.jdbc.ClientPreparedStatement.checkBounds(ClientPreparedStatement.java:1390)
[16:59:59 WARN]:        ... 15 more
  - type: textarea
    id: configuration_files
    attributes:
      label: Other files, you can drag and drop them here to upload. (optional)
      description: "Drag and drop your files here. Be careful not to upload a file that contains passwords or url of discord webhook"
  - type: textarea
    id: screenshots
    attributes:
      label: Screenshots/Videos (you can drag and drop files or paste links)
      description: "If applicable, add screenshots to help explain your problem (you can drag and drop files or paste links)."
  - type: markdown
    attributes:
      value: |
        ## Thanks for taking the time to fill out this bug report!