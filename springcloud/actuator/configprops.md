{
	"spring.jpa-org.springframework.boot.autoconfigure.orm.jpa.JpaProperties": {
		"prefix": "spring.jpa",
		"properties": {
			"error": "Cannot serialize 'spring.jpa'"
		}
	},
	"endpoints-org.springframework.boot.actuate.endpoint.EndpointProperties": {
		"prefix": "endpoints",
		"properties": {
			"enabled": true,
			"sensitive": null
		}
	},
	"management.info-org.springframework.boot.actuate.autoconfigure.InfoContributorProperties": {
		"prefix": "management.info",
		"properties": {
			"git": {
				"mode": "SIMPLE"
			}
		}
	},
	"metricsEndpoint": {
		"prefix": "endpoints.metrics",
		"properties": {
			"id": "metrics",
			"sensitive": true,
			"enabled": true
		}
	},
	"spring.jta-org.springframework.boot.autoconfigure.transaction.jta.JtaProperties": {
		"prefix": "spring.jta",
		"properties": {
			"logDir": null,
			"transactionManagerId": null
		}
	},
	"spring.jackson-org.springframework.boot.autoconfigure.jackson.JacksonProperties": {
		"prefix": "spring.jackson",
		"properties": {
			"propertyNamingStrategy": null,
			"defaultPropertyInclusion": null,
			"dateFormat": null,
			"timeZone": null,
			"locale": null,
			"serializationInclusion": null,
			"jodaDateTimeFormat": null
		}
	},
	"heapdumpMvcEndpoint": {
		"prefix": "endpoints.heapdump",
		"properties": {
			"path": "/heapdump",
			"sensitive": true,
			"enabled": true
		}
	},
	"endpoints.cors-org.springframework.boot.actuate.autoconfigure.EndpointCorsProperties": {
		"prefix": "endpoints.cors",
		"properties": {
			"allowedOrigins": [],
			"maxAge": 1800,
			"exposedHeaders": [],
			"allowedHeaders": [],
			"allowedMethods": [],
			"allowCredentials": null
		}
	},
	"environmentMvcEndpoint": {
		"prefix": "endpoints.env",
		"properties": {
			"path": "/env"
		}
	},
	"environmentEndpoint": {
		"prefix": "endpoints.env",
		"properties": {
			"id": "env",
			"sensitive": true,
			"enabled": true
		}
	},
	"spring.http.multipart-org.springframework.boot.autoconfigure.web.MultipartProperties": {
		"prefix": "spring.http.multipart",
		"properties": {
			"maxRequestSize": "10MB",
			"fileSizeThreshold": "0",
			"location": null,
			"maxFileSize": "1MB",
			"enabled": true,
			"resolveLazily": false
		}
	},
	"spring.info-org.springframework.boot.autoconfigure.info.ProjectInfoProperties": {
		"prefix": "spring.info",
		"properties": {
			"build": {
				"location": {
					
				}
			},
			"git": {
				"location": {
					
				}
			}
		}
	},
	"spring.datasource-org.springframework.boot.autoconfigure.jdbc.DataSourceProperties": {
		"prefix": "spring.datasource",
		"properties": {
			"schema": "classpath:schema.sql",
			"dataPassword": null,
			"data": "classpath:data.sql",
			"dataUsername": null,
			"generateUniqueName": false,
			"xa": {
				"dataSourceClassName": null,
				"properties": {
					
				}
			},
			"type": null,
			"separator": ";",
			"url": null,
			"platform": "h2",
			"continueOnError": false,
			"jndiName": null,
			"sqlScriptEncoding": null,
			"password": null,
			"schemaPassword": null,
			"name": "testdb",
			"driverClassName": null,
			"initialize": true,
			"schemaUsername": null,
			"username": null
		}
	},
	"traceEndpoint": {
		"prefix": "endpoints.trace",
		"properties": {
			"id": "trace",
			"sensitive": true,
			"enabled": true
		}
	},
	"metricsMvcEndpoint": {
		"prefix": "endpoints.metrics",
		"properties": {
			"path": "/metrics"
		}
	},
	"infoEndpoint": {
		"prefix": "endpoints.info",
		"properties": {
			"id": "info",
			"sensitive": false,
			"enabled": true
		}
	},
	"management.trace-org.springframework.boot.actuate.trace.TraceProperties": {
		"prefix": "management.trace",
		"properties": {
			"include": ["COOKIES",
			"REQUEST_HEADERS",
			"RESPONSE_HEADERS",
			"ERRORS"]
		}
	},
	"spring.resources-org.springframework.boot.autoconfigure.web.ResourceProperties": {
		"prefix": "spring.resources",
		"properties": {
			"cachePeriod": null,
			"addMappings": true,
			"chain": {
				"cache": true,
				"htmlApplicationCache": false,
				"gzipped": false,
				"strategy": {
					"fixed": {
						"enabled": false,
						"paths": ["/**"],
						"version": null
					},
					"content": {
						"enabled": false,
						"paths": ["/**"]
					}
				}
			},
			"staticLocations": ["/",
			"classpath:/META-INF/resources/",
			"classpath:/resources/",
			"classpath:/static/",
			"classpath:/public/"]
		}
	},
	"management.health.status-org.springframework.boot.actuate.autoconfigure.HealthIndicatorProperties": {
		"prefix": "management.health.status",
		"properties": {
			"order": null
		}
	},
	"healthMvcEndpoint": {
		"prefix": "endpoints.health",
		"properties": {
			"path": "/health"
		}
	},
	"serverProperties": {
		"prefix": "server",
		"properties": {
			"address": null,
			"maxHttpPostSize": 0,
			"undertow": {
				"bufferSize": null,
				"buffersPerRegion": null,
				"ioThreads": null,
				"workerThreads": null,
				"directBuffers": null,
				"accesslog": {
					"enabled": null,
					"pattern": "common",
					"prefix": "access_log.",
					"suffix": "log",
					"dir": "G:\\spring_cloud\\microservice_simple_provider_user\\logs"
				}
			},
			"tomcat": {
				"accesslog": {
					"enabled": false,
					"pattern": "common",
					"directory": "logs",
					"prefix": "access_log",
					"suffix": ".log",
					"renameOnRotate": false,
					"requestAttributesEnabled": false
				},
				"internalProxies": "10\\.\\d{1,3}\\.\\d{1,3}\\.\\d{1,3}|192\\.168\\.\\d{1,3}\\.\\d{1,3}|169\\.254\\.\\d{1,3}\\.\\d{1,3}|127\\.\\d{1,3}\\.\\d{1,3}\\.\\d{1,3}|172\\.1[6-9]{1}\\.\\d{1,3}\\.\\d{1,3}|172\\.2[0-9]{1}\\.\\d{1,3}\\.\\d{1,3}|172\\.3[0-1]{1}\\.\\d{1,3}\\.\\d{1,3}",
				"protocolHeader": null,
				"protocolHeaderHttpsValue": "https",
				"portHeader": "X-Forwarded-Port",
				"remoteIpHeader": null,
				"basedir": null,
				"backgroundProcessorDelay": 30,
				"maxThreads": 0,
				"minSpareThreads": 0,
				"maxHttpHeaderSize": 0,
				"redirectContextRoot": null,
				"uriEncoding": null
			},
			"displayName": "application",
			"session": {
				"timeout": null,
				"trackingModes": null,
				"persistent": false,
				"storeDir": null,
				"cookie": {
					"name": null,
					"domain": null,
					"path": null,
					"comment": null,
					"httpOnly": null,
					"secure": null,
					"maxAge": null
				}
			},
			"contextPath": null,
			"error": {
				"path": "/error",
				"includeStacktrace": "NEVER"
			},
			"ssl": null,
			"serverHeader": null,
			"useForwardHeaders": null,
			"port": 8080,
			"maxHttpHeaderSize": 0,
			"servletPath": "/",
			"jspServlet": null,
			"jetty": {
				"acceptors": null,
				"selectors": null
			},
			"connectionTimeout": null
		}
	},
	"spring.metrics.export-org.springframework.boot.actuate.metrics.export.MetricExportProperties": {
		"prefix": "spring.metrics.export",
		"properties": {
			"excludes": null,
			"statsd": {
				"host": null,
				"port": 8125,
				"prefix": null
			},
			"includes": null,
			"enabled": true,
			"redis": {
				"prefix": "spring.metrics.application.163913ee6063d57752a90efef723749f",
				"key": "******"
			},
			"aggregate": {
				"prefix": "application.163913ee6063d57752a90efef723749f",
				"keyPattern": "k.d"
			}
		}
	},
	"configurationPropertiesReportEndpoint": {
		"prefix": "endpoints.configprops",
		"properties": {
			"id": "configprops",
			"sensitive": true,
			"enabled": true
		}
	},
	"healthEndpoint": {
		"prefix": "endpoints.health",
		"properties": {
			"timeToLive": 1000,
			"id": "health",
			"sensitive": false,
			"enabled": true
		}
	},
	"endpoints.metrics.filter-org.springframework.boot.actuate.autoconfigure.MetricFilterProperties": {
		"prefix": "endpoints.metrics.filter",
		"properties": {
			"counterSubmissions": ["MERGED"],
			"gaugeSubmissions": ["MERGED"]
		}
	},
	"dumpEndpoint": {
		"prefix": "endpoints.dump",
		"properties": {
			"id": "dump",
			"sensitive": true,
			"enabled": true
		}
	},
	"autoConfigurationReportEndpoint": {
		"prefix": "endpoints.autoconfig",
		"properties": {
			"id": "autoconfig",
			"sensitive": true,
			"enabled": true
		}
	},
	"endpoints.jmx-org.springframework.boot.actuate.autoconfigure.EndpointMBeanExportProperties": {
		"prefix": "endpoints.jmx",
		"properties": {
			"uniqueNames": false,
			"enabled": true,
			"domain": ""
		}
	},
	"spring.http.encoding-org.springframework.boot.autoconfigure.web.HttpEncodingProperties": {
		"prefix": "spring.http.encoding",
		"properties": {
			"charset": "UTF-8",
			"force": false,
			"mapping": null,
			"forceRequest": false,
			"forceResponse": false
		}
	},
	"shutdownEndpoint": {
		"prefix": "endpoints.shutdown",
		"properties": {
			"id": "shutdown",
			"sensitive": true,
			"enabled": false
		}
	},
	"beansEndpoint": {
		"prefix": "endpoints.beans",
		"properties": {
			"id": "beans",
			"sensitive": true,
			"enabled": true
		}
	},
	"managementServerProperties": {
		"prefix": "management",
		"properties": {
			"security": {
				"enabled": true,
				"roles": ["ADMIN"],
				"sessions": "STATELESS"
			},
			"address": null,
			"port": null,
			"addApplicationContextHeader": true,
			"contextPath": "",
			"ssl": null
		}
	},
	"requestMappingEndpoint": {
		"prefix": "endpoints.mappings",
		"properties": {
			"id": "mappings",
			"sensitive": true,
			"enabled": true
		}
	},
	"endpoints.health-org.springframework.boot.actuate.autoconfigure.HealthMvcEndpointProperties": {
		"prefix": "endpoints.health",
		"properties": {
			"mapping": {
				
			}
		}
	},
	"dataSource": {
		"prefix": "spring.datasource.tomcat",
		"properties": {
			"connectionProperties": null,
			"propagateInterruptState": false,
			"validator": null,
			"useDisposableConnectionFacade": true,
			"defaultCatalog": null,
			"validationInterval": 3000,
			"jmxEnabled": true,
			"ignoreExceptionOnPreLoad": false,
			"logAbandoned": false,
			"commitOnReturn": false,
			"password": "******",
			"maxIdle": 100,
			"testWhileIdle": false,
			"removeAbandoned": false,
			"poolProperties": {
				"dbProperties": {
					"user": "sa",
					"password": "******"
				},
				"url": "jdbc:h2:mem:testdb;DB_CLOSE_DELAY=-1;DB_CLOSE_ON_EXIT=FALSE",
				"driverClassName": "org.h2.Driver",
				"defaultAutoCommit": null,
				"defaultReadOnly": null,
				"defaultTransactionIsolation": -1,
				"defaultCatalog": null,
				"connectionProperties": null,
				"initialSize": 10,
				"maxActive": 100,
				"maxIdle": 100,
				"minIdle": 10,
				"maxWait": 30000,
				"validationQuery": "SELECT 1",
				"validationQueryTimeout": -1,
				"validatorClassName": null,
				"validator": null,
				"testOnBorrow": true,
				"testOnReturn": false,
				"testWhileIdle": false,
				"timeBetweenEvictionRunsMillis": 5000,
				"numTestsPerEvictionRun": 0,
				"minEvictableIdleTimeMillis": 60000,
				"accessToUnderlyingConnectionAllowed": true,
				"removeAbandoned": false,
				"removeAbandonedTimeout": 60,
				"logAbandoned": false,
				"name": "Tomcat Connection Pool[1-809400262]",
				"password": "******",
				"username": "sa",
				"validationInterval": 3000,
				"jmxEnabled": true,
				"initSQL": null,
				"testOnConnect": false,
				"jdbcInterceptors": null,
				"fairQueue": true,
				"useEquals": true,
				"abandonWhenPercentageFull": 0,
				"maxAge": 0,
				"useLock": false,
				"suspectTimeout": 0,
				"dataSource": null,
				"dataSourceJNDI": null,
				"alternateUsernameAllowed": false,
				"commitOnReturn": false,
				"rollbackOnReturn": false,
				"useDisposableConnectionFacade": true,
				"logValidationErrors": false,
				"propagateInterruptState": false,
				"ignoreExceptionOnPreLoad": false
			},
			"minIdle": 10,
			"abandonWhenPercentageFull": 0,
			"defaultReadOnly": null,
			"pool": {
				"poolProperties": {
					"dbProperties": {
						"user": "sa",
						"password": "******"
					},
					"url": "jdbc:h2:mem:testdb;DB_CLOSE_DELAY=-1;DB_CLOSE_ON_EXIT=FALSE",
					"driverClassName": "org.h2.Driver",
					"defaultAutoCommit": null,
					"defaultReadOnly": null,
					"defaultTransactionIsolation": -1,
					"defaultCatalog": null,
					"connectionProperties": null,
					"initialSize": 10,
					"maxActive": 100,
					"maxIdle": 100,
					"minIdle": 10,
					"maxWait": 30000,
					"validationQuery": "SELECT 1",
					"validationQueryTimeout": -1,
					"validatorClassName": null,
					"validator": null,
					"testOnBorrow": true,
					"testOnReturn": false,
					"testWhileIdle": false,
					"timeBetweenEvictionRunsMillis": 5000,
					"numTestsPerEvictionRun": 0,
					"minEvictableIdleTimeMillis": 60000,
					"accessToUnderlyingConnectionAllowed": true,
					"removeAbandoned": false,
					"removeAbandonedTimeout": 60,
					"logAbandoned": false,
					"name": "Tomcat Connection Pool[1-809400262]",
					"password": "******",
					"username": "sa",
					"validationInterval": 3000,
					"jmxEnabled": true,
					"initSQL": null,
					"testOnConnect": false,
					"jdbcInterceptors": null,
					"fairQueue": true,
					"useEquals": true,
					"abandonWhenPercentageFull": 0,
					"maxAge": 0,
					"useLock": false,
					"suspectTimeout": 0,
					"dataSource": null,
					"dataSourceJNDI": null,
					"alternateUsernameAllowed": false,
					"commitOnReturn": false,
					"rollbackOnReturn": false,
					"useDisposableConnectionFacade": true,
					"logValidationErrors": false,
					"propagateInterruptState": false,
					"ignoreExceptionOnPreLoad": false
				}
			},
			"maxWait": 30000,
			"logValidationErrors": false,
			"name": "Tomcat Connection Pool[1-809400262]",
			"driverClassName": "org.h2.Driver",
			"dataSource": null,
			"initSQL": null,
			"validationQueryTimeout": -1,
			"dbProperties": {
				"user": "sa",
				"password": "******"
			},
			"validationQuery": "SELECT 1",
			"rollbackOnReturn": false,
			"logWriter": null,
			"validatorClassName": null,
			"dataSourceJNDI": null,
			"alternateUsernameAllowed": false,
			"suspectTimeout": 0,
			"useEquals": true,
			"removeAbandonedTimeout": 60,
			"defaultAutoCommit": null,
			"loginTimeout": 30,
			"testOnConnect": false,
			"jdbcInterceptors": null,
			"initialSize": 10,
			"defaultTransactionIsolation": -1,
			"url": "jdbc:h2:mem:testdb;DB_CLOSE_DELAY=-1;DB_CLOSE_ON_EXIT=FALSE",
			"numTestsPerEvictionRun": 0,
			"testOnBorrow": true,
			"fairQueue": true,
			"maxAge": 0,
			"minEvictableIdleTimeMillis": 60000,
			"timeBetweenEvictionRunsMillis": 5000,
			"accessToUnderlyingConnectionAllowed": true,
			"testOnReturn": false,
			"useLock": false,
			"username": "sa",
			"maxActive": 100
		}
	},
	"spring.mvc-org.springframework.boot.autoconfigure.web.WebMvcProperties": {
		"prefix": "spring.mvc",
		"properties": {
			"dateFormat": null,
			"servlet": {
				"loadOnStartup": -1
			},
			"staticPathPattern": "/**",
			"dispatchOptionsRequest": true,
			"dispatchTraceRequest": false,
			"locale": null,
			"ignoreDefaultModelOnRedirect": true,
			"logResolvedException": false,
			"async": {
				"requestTimeout": null
			},
			"messageCodesResolverFormat": null,
			"mediaTypes": {
				
			},
			"view": {
				"prefix": null,
				"suffix": null
			},
			"localeResolver": "ACCEPT_HEADER",
			"throwExceptionIfNoHandlerFound": false
		}
	},
	"diskSpaceHealthIndicatorProperties": {
		"prefix": "management.health.diskspace",
		"properties": {
			"path": "G:\\spring_cloud\\microservice_simple_provider_user\\.",
			"threshold": 10485760
		}
	}
}