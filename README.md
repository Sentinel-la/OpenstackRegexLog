# OpenstackRegexLog
Regular expression to parse openstack logs

### Example

1.- The following  DEBU log:  

2016-01-04 22:41:36.297 DEBUG oslo_db.sqlalchemy.engines [req-af32b586-0aab-4846-b097-12604699d5ec None None] MySQL server mode set to STRICT_TRANS_TABLES,STRICT_ALL_TABLES,NO_ZERO_IN_DATE,NO_ZERO_DATE,ERROR_FOR_DIVISION_BY_ZERO,TRADITIONAL,NO_AUTO_CREATE_USER,NO_ENGINE_SUBSTITUTION _check_effective_sql_mode /usr/local/lib/python2.7/dist-packages/oslo_db/sqlalchemy/engines.py:256  


Parsed and stored as json:

{  
    "time" : "2016-01-04 22:41:36.297",  
    "description" : "[req-af32b586-0aab-4846-b097-12604699d5ec None None] MySQL server mode set to STRICT_TRANS_TABLES,STRICT_ALL_TABLES,NO_ZERO_IN_DATE,NO_ZERO_DATE,ERROR_FOR_DIVISION_BY_ZERO,TRADITIONAL,NO_AUTO_CREATE_USER,NO_ENGINE_SUBSTITUTION _check_effective_sql_mode /usr/local/lib/python2.7/dist-packages/oslo_db/sqlalchemy/engines.py:256",  
    "level" : "DEBUG",  
    "log_id" : null,  
    "component" : "oslo_db.sqlalchemy.engines ",  
}  

2.- The following  WARNING log:  

2016-01-04 22:41:35.221 19090 WARNING oslo_config.cfg [-] Option "username" from group "keystone_authtoken" is deprecated. Use option "user-name" from group "keystone_authtoken".  


Parsed and stored as json:  

{  
    "time" : "2016-01-04 22:41:35.221",  
    "description" : "[-] Option "username" from group "keystone_authtoken" is deprecated. Use option "user-name" from group "keystone_authtoken",  
    "level" : "WARNING",  
    "log_id" : 19090,  
    "component" : "oslo_config.cfg",  
}  

