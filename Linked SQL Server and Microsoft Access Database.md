--Create linked server with access password protected file Microsoft.ACE.OLEDB.12.0 Driver

exec sp_addlinkedserver

    @server = 'GIGASOFT',

    @provider = 'Microsoft.ACE.OLEDB.12.0',

    @srvproduct = 'GIGASOFT',

    @datasrc = 'C:\SOFTWAREMEN\Suit\Shared Resources\GIGASOFT.MDB',

    @provstr = ';PWD=XXXX'

 

exec sp_addlinkedsrvlogin

    @rmtsrvname = 'GIGASOFT',

    @useself = 'FALSE',

    @locallogin = null,

    @rmtuser = 'Admin',

    @rmtpassword = null

 

--Create linked server with access password protected file Microsoft.ODBC Driver

exec sp_addlinkedserver

    @server = 'GIGASOFT1',

    @provider = 'MSDASQL',

    @srvproduct = 'GIGASOFT',

    @datasrc = 'GIGASOFT',

    @provstr = ';PWD=XXXX'

 

exec sp_addlinkedsrvlogin

    @rmtsrvname = 'GIGASOFT1',

    @useself = 'FALSE',

    @locallogin = null,

    @rmtuser = 'Admin',

    @rmtpassword = 'XXXX'
