{
	"positiveMatches": {
		"AuditAutoConfiguration#auditListener": [{
			"condition": "OnBeanCondition",
			"message": "@ConditionalOnMissingBean (types: org.springframework.boot.actuate.audit.listener.AbstractAuditListener; SearchStrategy: all) did not find any beans"
		}],
		"AuditAutoConfiguration.AuditEventRepositoryConfiguration": [{
			"condition": "OnBeanCondition",
			"message": "@ConditionalOnMissingBean (types: org.springframework.boot.actuate.audit.AuditEventRepository; SearchStrategy: all) did not find any beans"
		}],
		"EndpointAutoConfiguration#autoConfigurationReportEndpoint": [{
			"condition": "OnBeanCondition",
			"message": "@ConditionalOnBean (types: org.springframework.boot.autoconfigure.condition.ConditionEvaluationReport; SearchStrategy: all) found bean 'autoConfigurationReport'; @ConditionalOnMissingBean (types: org.springframework.boot.actuate.endpoint.AutoConfigurationReportEndpoint; SearchStrategy: current) did not find any beans"
		}],
		"EndpointAutoConfiguration#beansEndpoint": [{
			"condition": "OnBeanCondition",
			"message": "@ConditionalOnMissingBean (types: org.springframework.boot.actuate.endpoint.BeansEndpoint; SearchStrategy: all) did not find any beans"
		}],
		"EndpointAutoConfiguration#configurationPropertiesReportEndpoint": [{
			"condition": "OnBeanCondition",
			"message": "@ConditionalOnMissingBean (types: org.springframework.boot.actuate.endpoint.ConfigurationPropertiesReportEndpoint; SearchStrategy: all) did not find any beans"
		}],
		"EndpointAutoConfiguration#dumpEndpoint": [{
			"condition": "OnBeanCondition",
			"message": "@ConditionalOnMissingBean (types: org.springframework.boot.actuate.endpoint.DumpEndpoint; SearchStrategy: all) did not find any beans"
		}],
		"EndpointAutoConfiguration#environmentEndpoint": [{
			"condition": "OnBeanCondition",
			"message": "@ConditionalOnMissingBean (types: org.springframework.boot.actuate.endpoint.EnvironmentEndpoint; SearchStrategy: all) did not find any beans"
		}],
		"EndpointAutoConfiguration#healthEndpoint": [{
			"condition": "OnBeanCondition",
			"message": "@ConditionalOnMissingBean (types: org.springframework.boot.actuate.endpoint.HealthEndpoint; SearchStrategy: all) did not find any beans"
		}],
		"EndpointAutoConfiguration#infoEndpoint": [{
			"condition": "OnBeanCondition",
			"message": "@ConditionalOnMissingBean (types: org.springframework.boot.actuate.endpoint.InfoEndpoint; SearchStrategy: all) did not find any beans"
		}],
		"EndpointAutoConfiguration#metricsEndpoint": [{
			"condition": "OnBeanCondition",
			"message": "@ConditionalOnMissingBean (types: org.springframework.boot.actuate.endpoint.MetricsEndpoint; SearchStrategy: all) did not find any beans"
		}],
		"EndpointAutoConfiguration#shutdownEndpoint": [{
			"condition": "OnBeanCondition",
			"message": "@ConditionalOnMissingBean (types: org.springframework.boot.actuate.endpoint.ShutdownEndpoint; SearchStrategy: all) did not find any beans"
		}],
		"EndpointAutoConfiguration#traceEndpoint": [{
			"condition": "OnBeanCondition",
			"message": "@ConditionalOnMissingBean (types: org.springframework.boot.actuate.endpoint.TraceEndpoint; SearchStrategy: all) did not find any beans"
		}],
		"EndpointAutoConfiguration.RequestMappingEndpointConfiguration": [{
			"condition": "OnClassCondition",
			"message": "@ConditionalOnClass found required class 'org.springframework.web.servlet.handler.AbstractHandlerMethodMapping'"
		}],
		"EndpointAutoConfiguration.RequestMappingEndpointConfiguration#requestMappingEndpoint": [{
			"condition": "OnBeanCondition",
			"message": "@ConditionalOnMissingBean (types: org.springframework.boot.actuate.endpoint.RequestMappingEndpoint; SearchStrategy: all) did not find any beans"
		}],
		"EndpointMBeanExportAutoConfiguration": [{
			"condition": "EndpointMBeanExportAutoConfiguration.JmxEnabledCondition",
			"message": "JMX Enabled found properties spring.jmx.enabled, endpoints.jmx.enabled"
		}],
		"EndpointWebMvcAutoConfiguration": [{
			"condition": "OnClassCondition",
			"message": "@ConditionalOnClass found required classes 'javax.servlet.Servlet', 'org.springframework.web.servlet.DispatcherServlet'"
		},
		{
			"condition": "OnWebApplicationCondition",
			"message": "@ConditionalOnWebApplication (required) found StandardServletEnvironment"
		}],
		"EndpointWebMvcAutoConfiguration.ApplicationContextFilterConfiguration": [{
			"condition": "OnPropertyCondition",
			"message": "@ConditionalOnProperty (management.add-application-context-header=true) matched"
		}],
		"EndpointWebMvcAutoConfiguration.EndpointWebMvcConfiguration": [{
			"condition": "EndpointWebMvcAutoConfiguration.OnManagementMvcCondition",
			"message": "Management Server MVC port is same"
		}],
		"EndpointWebMvcManagementContextConfiguration#endpointHandlerMapping": [{
			"condition": "OnBeanCondition",
			"message": "@ConditionalOnMissingBean (types: org.springframework.boot.actuate.endpoint.mvc.EndpointHandlerMapping; SearchStrategy: all) did not find any beans"
		}],
		"EndpointWebMvcManagementContextConfiguration#environmentMvcEndpoint": [{
			"condition": "OnBeanCondition",
			"message": "@ConditionalOnBean (types: org.springframework.boot.actuate.endpoint.EnvironmentEndpoint; SearchStrategy: all) found bean 'environmentEndpoint'"
		},
		{
			"condition": "OnEnabledEndpointCondition",
			"message": "@ConditionalOnEnabledEndpoint All endpoints are enabled by default"
		}],
		"EndpointWebMvcManagementContextConfiguration#healthMvcEndpoint": [{
			"condition": "OnBeanCondition",
			"message": "@ConditionalOnBean (types: org.springframework.boot.actuate.endpoint.HealthEndpoint; SearchStrategy: all) found bean 'healthEndpoint'"
		},
		{
			"condition": "OnEnabledEndpointCondition",
			"message": "@ConditionalOnEnabledEndpoint All endpoints are enabled by default"
		}],
		"EndpointWebMvcManagementContextConfiguration#heapdumpMvcEndpoint": [{
			"condition": "OnBeanCondition",
			"message": "@ConditionalOnMissingBean (types: org.springframework.boot.actuate.endpoint.mvc.HeapdumpMvcEndpoint; SearchStrategy: all) did not find any beans"
		},
		{
			"condition": "OnEnabledEndpointCondition",
			"message": "@ConditionalOnEnabledEndpoint All endpoints are enabled by default"
		}],
		"EndpointWebMvcManagementContextConfiguration#metricsMvcEndpoint": [{
			"condition": "OnBeanCondition",
			"message": "@ConditionalOnBean (types: org.springframework.boot.actuate.endpoint.MetricsEndpoint; SearchStrategy: all) found bean 'metricsEndpoint'"
		},
		{
			"condition": "OnEnabledEndpointCondition",
			"message": "@ConditionalOnEnabledEndpoint All endpoints are enabled by default"
		}],
		"EndpointWebMvcManagementContextConfiguration#mvcEndpoints": [{
			"condition": "OnBeanCondition",
			"message": "@ConditionalOnMissingBean (types: org.springframework.boot.actuate.endpoint.mvc.MvcEndpoints; SearchStrategy: all) did not find any beans"
		}],
		"HealthIndicatorAutoConfiguration#healthAggregator": [{
			"condition": "OnBeanCondition",
			"message": "@ConditionalOnMissingBean (types: org.springframework.boot.actuate.health.HealthAggregator; SearchStrategy: all) did not find any beans"
		}],
		"HealthIndicatorAutoConfiguration.DataSourcesHealthIndicatorConfiguration": [{
			"condition": "OnClassCondition",
			"message": "@ConditionalOnClass found required class 'org.springframework.jdbc.core.JdbcTemplate'"
		},
		{
			"condition": "OnEnabledHealthIndicatorCondition",
			"message": "@ConditionalOnEnabledHealthIndicator management.health.defaults.enabled is considered true"
		},
		{
			"condition": "OnBeanCondition",
			"message": "@ConditionalOnBean (types: javax.sql.DataSource; SearchStrategy: all) found bean 'dataSource'"
		}],
		"HealthIndicatorAutoConfiguration.DataSourcesHealthIndicatorConfiguration#dbHealthIndicator": [{
			"condition": "OnBeanCondition",
			"message": "@ConditionalOnMissingBean (names: dbHealthIndicator; SearchStrategy: all) did not find any beans"
		}],
		"HealthIndicatorAutoConfiguration.DiskSpaceHealthIndicatorConfiguration": [{
			"condition": "OnEnabledHealthIndicatorCondition",
			"message": "@ConditionalOnEnabledHealthIndicator management.health.defaults.enabled is considered true"
		}],
		"HealthIndicatorAutoConfiguration.DiskSpaceHealthIndicatorConfiguration#diskSpaceHealthIndicator": [{
			"condition": "OnBeanCondition",
			"message": "@ConditionalOnMissingBean (names: diskSpaceHealthIndicator; SearchStrategy: all) did not find any beans"
		}],
		"InfoContributorAutoConfiguration#envInfoContributor": [{
			"condition": "OnEnabledInfoContributorCondition",
			"message": "@ConditionalOnEnabledInfoContributor management.info.defaults.enabled is considered true"
		}],
		"ManagementServerPropertiesAutoConfiguration#managementServerProperties": [{
			"condition": "OnBeanCondition",
			"message": "@ConditionalOnMissingBean (types: org.springframework.boot.actuate.autoconfigure.ManagementServerProperties; SearchStrategy: all) did not find any beans"
		}],
		"MetricExportAutoConfiguration": [{
			"condition": "OnPropertyCondition",
			"message": "@ConditionalOnProperty (spring.metrics.export.enabled) matched"
		}],
		"MetricExportAutoConfiguration#metricWritersMetricExporter": [{
			"condition": "OnBeanCondition",
			"message": "@ConditionalOnMissingBean (names: metricWritersMetricExporter; SearchStrategy: all) did not find any beans"
		}],
		"MetricExportAutoConfiguration.MetricExportPropertiesConfiguration#metricExportProperties": [{
			"condition": "OnBeanCondition",
			"message": "@ConditionalOnMissingBean (types: org.springframework.boot.actuate.metrics.export.MetricExportProperties; SearchStrategy: all) did not find any beans"
		}],
		"MetricFilterAutoConfiguration": [{
			"condition": "OnClassCondition",
			"message": "@ConditionalOnClass found required classes 'javax.servlet.Servlet', 'javax.servlet.ServletRegistration', 'org.springframework.web.filter.OncePerRequestFilter', 'org.springframework.web.servlet.HandlerMapping'"
		},
		{
			"condition": "OnPropertyCondition",
			"message": "@ConditionalOnProperty (endpoints.metrics.filter.enabled) matched"
		},
		{
			"condition": "OnBeanCondition",
			"message": "@ConditionalOnBean (types: org.springframework.boot.actuate.metrics.CounterService,org.springframework.boot.actuate.metrics.GaugeService; SearchStrategy: all) found beans 'counterService', 'gaugeService'"
		}],
		"MetricRepositoryAutoConfiguration.FastMetricServicesConfiguration": [{
			"condition": "OnJavaCondition",
			"message": "@ConditionalOnJava (1.8 or newer) found 1.8"
		},
		{
			"condition": "OnBeanCondition",
			"message": "@ConditionalOnMissingBean (types: org.springframework.boot.actuate.metrics.GaugeService; SearchStrategy: all) did not find any beans"
		}],
		"MetricRepositoryAutoConfiguration.FastMetricServicesConfiguration#actuatorMetricReader": [{
			"condition": "OnBeanCondition",
			"message": "@ConditionalOnMissingBean (types: org.springframework.boot.actuate.metrics.buffer.BufferMetricReader; SearchStrategy: all) did not find any beans"
		}],
		"MetricRepositoryAutoConfiguration.FastMetricServicesConfiguration#counterBuffers": [{
			"condition": "OnBeanCondition",
			"message": "@ConditionalOnMissingBean (types: org.springframework.boot.actuate.metrics.buffer.CounterBuffers; SearchStrategy: all) did not find any beans"
		}],
		"MetricRepositoryAutoConfiguration.FastMetricServicesConfiguration#counterService": [{
			"condition": "OnBeanCondition",
			"message": "@ConditionalOnMissingBean (types: org.springframework.boot.actuate.metrics.CounterService; SearchStrategy: all) did not find any beans"
		}],
		"MetricRepositoryAutoConfiguration.FastMetricServicesConfiguration#gaugeBuffers": [{
			"condition": "OnBeanCondition",
			"message": "@ConditionalOnMissingBean (types: org.springframework.boot.actuate.metrics.buffer.GaugeBuffers; SearchStrategy: all) did not find any beans"
		}],
		"MetricRepositoryAutoConfiguration.FastMetricServicesConfiguration#gaugeService": [{
			"condition": "OnBeanCondition",
			"message": "@ConditionalOnMissingBean (types: org.springframework.boot.actuate.metrics.GaugeService; SearchStrategy: all) did not find any beans"
		}],
		"PublicMetricsAutoConfiguration.DataSourceMetricsConfiguration": [{
			"condition": "OnClassCondition",
			"message": "@ConditionalOnClass found required class 'javax.sql.DataSource'"
		},
		{
			"condition": "OnBeanCondition",
			"message": "@ConditionalOnBean (types: javax.sql.DataSource; SearchStrategy: all) found bean 'dataSource'"
		}],
		"PublicMetricsAutoConfiguration.DataSourceMetricsConfiguration#dataSourcePublicMetrics": [{
			"condition": "OnBeanCondition",
			"message": "@ConditionalOnBean (types: org.springframework.boot.autoconfigure.jdbc.metadata.DataSourcePoolMetadataProvider; SearchStrategy: all) found bean 'tomcatPoolDataSourceMetadataProvider'; @ConditionalOnMissingBean (types: org.springframework.boot.actuate.endpoint.DataSourcePublicMetrics; SearchStrategy: all) did not find any beans"
		}],
		"PublicMetricsAutoConfiguration.TomcatMetricsConfiguration": [{
			"condition": "OnClassCondition",
			"message": "@ConditionalOnClass found required classes 'javax.servlet.Servlet', 'org.apache.catalina.startup.Tomcat'"
		},
		{
			"condition": "OnWebApplicationCondition",
			"message": "@ConditionalOnWebApplication (required) found StandardServletEnvironment"
		}],
		"PublicMetricsAutoConfiguration.TomcatMetricsConfiguration#tomcatPublicMetrics": [{
			"condition": "OnBeanCondition",
			"message": "@ConditionalOnMissingBean (types: org.springframework.boot.actuate.endpoint.TomcatPublicMetrics; SearchStrategy: all) did not find any beans"
		}],
		"TraceRepositoryAutoConfiguration#traceRepository": [{
			"condition": "OnBeanCondition",
			"message": "@ConditionalOnMissingBean (types: org.springframework.boot.actuate.trace.TraceRepository; SearchStrategy: all) did not find any beans"
		}],
		"TraceWebFilterAutoConfiguration": [{
			"condition": "OnClassCondition",
			"message": "@ConditionalOnClass found required classes 'javax.servlet.Servlet', 'org.springframework.web.servlet.DispatcherServlet', 'javax.servlet.ServletRegistration'"
		}],
		"TraceWebFilterAutoConfiguration#webRequestLoggingFilter": [{
			"condition": "OnBeanCondition",
			"message": "@ConditionalOnMissingBean (types: org.springframework.boot.actuate.trace.WebRequestTraceFilter; SearchStrategy: all) did not find any beans"
		}],
		"PropertyPlaceholderAutoConfiguration#propertySourcesPlaceholderConfigurer": [{
			"condition": "OnBeanCondition",
			"message": "@ConditionalOnMissingBean (types: org.springframework.context.support.PropertySourcesPlaceholderConfigurer; SearchStrategy: current) did not find any beans"
		}],
		"AopAutoConfiguration": [{
			"condition": "OnClassCondition",
			"message": "@ConditionalOnClass found required classes 'org.springframework.context.annotation.EnableAspectJAutoProxy', 'org.aspectj.lang.annotation.Aspect', 'org.aspectj.lang.reflect.Advice'"
		},
		{
			"condition": "OnPropertyCondition",
			"message": "@ConditionalOnProperty (spring.aop.auto=true) matched"
		}],
		"AopAutoConfiguration.JdkDynamicAutoProxyConfiguration": [{
			"condition": "OnPropertyCondition",
			"message": "@ConditionalOnProperty (spring.aop.proxy-target-class=false) matched"
		}],
		"GenericCacheConfiguration": [{
			"condition": "CacheCondition",
			"message": "Cache org.springframework.boot.autoconfigure.cache.GenericCacheConfiguration automatic cache type"
		}],
		"NoOpCacheConfiguration": [{
			"condition": "CacheCondition",
			"message": "Cache org.springframework.boot.autoconfigure.cache.NoOpCacheConfiguration automatic cache type"
		}],
		"RedisCacheConfiguration": [{
			"condition": "CacheCondition",
			"message": "Cache org.springframework.boot.autoconfigure.cache.RedisCacheConfiguration automatic cache type"
		}],
		"SimpleCacheConfiguration": [{
			"condition": "CacheCondition",
			"message": "Cache org.springframework.boot.autoconfigure.cache.SimpleCacheConfiguration automatic cache type"
		}],
		"PersistenceExceptionTranslationAutoConfiguration": [{
			"condition": "OnClassCondition",
			"message": "@ConditionalOnClass found required class 'org.springframework.dao.annotation.PersistenceExceptionTranslationPostProcessor'"
		}],
		"PersistenceExceptionTranslationAutoConfiguration#persistenceExceptionTranslationPostProcessor": [{
			"condition": "OnPropertyCondition",
			"message": "@ConditionalOnProperty (spring.dao.exceptiontranslation.enabled) matched"
		},
		{
			"condition": "OnBeanCondition",
			"message": "@ConditionalOnMissingBean (types: org.springframework.dao.annotation.PersistenceExceptionTranslationPostProcessor; SearchStrategy: all) did not find any beans"
		}],
		"JpaRepositoriesAutoConfiguration": [{
			"condition": "OnClassCondition",
			"message": "@ConditionalOnClass found required class 'org.springframework.data.jpa.repository.JpaRepository'"
		},
		{
			"condition": "OnPropertyCondition",
			"message": "@ConditionalOnProperty (spring.data.jpa.repositories.enabled=true) matched"
		},
		{
			"condition": "OnBeanCondition",
			"message": "@ConditionalOnBean (types: javax.sql.DataSource; SearchStrategy: all) found bean 'dataSource'; @ConditionalOnMissingBean (types: org.springframework.data.jpa.repository.support.JpaRepositoryFactoryBean,org.springframework.data.jpa.repository.config.JpaRepositoryConfigExtension; SearchStrategy: all) did not find any beans"
		}],
		"SpringDataWebAutoConfiguration": [{
			"condition": "OnClassCondition",
			"message": "@ConditionalOnClass found required classes 'org.springframework.data.web.PageableHandlerMethodArgumentResolver', 'org.springframework.web.servlet.config.annotation.WebMvcConfigurerAdapter'"
		},
		{
			"condition": "OnWebApplicationCondition",
			"message": "@ConditionalOnWebApplication (required) found StandardServletEnvironment"
		},
		{
			"condition": "OnBeanCondition",
			"message": "@ConditionalOnMissingBean (types: org.springframework.data.web.PageableHandlerMethodArgumentResolver; SearchStrategy: all) did not find any beans"
		}],
		"JacksonAutoConfiguration": [{
			"condition": "OnClassCondition",
			"message": "@ConditionalOnClass found required class 'com.fasterxml.jackson.databind.ObjectMapper'"
		}],
		"JacksonAutoConfiguration.Jackson2ObjectMapperBuilderCustomizerConfiguration": [{
			"condition": "OnClassCondition",
			"message": "@ConditionalOnClass found required classes 'com.fasterxml.jackson.databind.ObjectMapper', 'org.springframework.http.converter.json.Jackson2ObjectMapperBuilder'"
		}],
		"JacksonAutoConfiguration.JacksonObjectMapperBuilderConfiguration": [{
			"condition": "OnClassCondition",
			"message": "@ConditionalOnClass found required classes 'com.fasterxml.jackson.databind.ObjectMapper', 'org.springframework.http.converter.json.Jackson2ObjectMapperBuilder'"
		}],
		"JacksonAutoConfiguration.JacksonObjectMapperBuilderConfiguration#jacksonObjectMapperBuilder": [{
			"condition": "OnBeanCondition",
			"message": "@ConditionalOnMissingBean (types: org.springframework.http.converter.json.Jackson2ObjectMapperBuilder; SearchStrategy: all) did not find any beans"
		}],
		"JacksonAutoConfiguration.JacksonObjectMapperConfiguration": [{
			"condition": "OnClassCondition",
			"message": "@ConditionalOnClass found required classes 'com.fasterxml.jackson.databind.ObjectMapper', 'org.springframework.http.converter.json.Jackson2ObjectMapperBuilder'"
		}],
		"JacksonAutoConfiguration.JacksonObjectMapperConfiguration#jacksonObjectMapper": [{
			"condition": "OnBeanCondition",
			"message": "@ConditionalOnMissingBean (types: com.fasterxml.jackson.databind.ObjectMapper; SearchStrategy: all) did not find any beans"
		}],
		"DataSourceAutoConfiguration": [{
			"condition": "OnClassCondition",
			"message": "@ConditionalOnClass found required classes 'javax.sql.DataSource', 'org.springframework.jdbc.datasource.embedded.EmbeddedDatabaseType'"
		}],
		"DataSourceAutoConfiguration#dataSourceInitializer": [{
			"condition": "OnBeanCondition",
			"message": "@ConditionalOnMissingBean (types: org.springframework.boot.autoconfigure.jdbc.DataSourceInitializer; SearchStrategy: all) did not find any beans"
		}],
		"DataSourceAutoConfiguration.PooledDataSourceConfiguration": [{
			"condition": "DataSourceAutoConfiguration.PooledDataSourceCondition",
			"message": "AnyNestedCondition 1 matched 1 did not; NestedCondition on DataSourceAutoConfiguration.PooledDataSourceCondition.PooledDataSourceAvailable PooledDataSource found supported DataSource; NestedCondition on DataSourceAutoConfiguration.PooledDataSourceCondition.ExplicitType @ConditionalOnProperty (spring.datasource.type) did not find property 'type'"
		},
		{
			"condition": "OnBeanCondition",
			"message": "@ConditionalOnMissingBean (types: javax.sql.DataSource,javax.sql.XADataSource; SearchStrategy: all) did not find any beans"
		}],
		"DataSourceConfiguration.Tomcat": [{
			"condition": "OnClassCondition",
			"message": "@ConditionalOnClass found required class 'org.apache.tomcat.jdbc.pool.DataSource'"
		},
		{
			"condition": "OnPropertyCondition",
			"message": "@ConditionalOnProperty (spring.datasource.type=org.apache.tomcat.jdbc.pool.DataSource) matched"
		}],
		"DataSourceTransactionManagerAutoConfiguration": [{
			"condition": "OnClassCondition",
			"message": "@ConditionalOnClass found required classes 'org.springframework.jdbc.core.JdbcTemplate', 'org.springframework.transaction.PlatformTransactionManager'"
		}],
		"DataSourceTransactionManagerAutoConfiguration.DataSourceTransactionManagerConfiguration": [{
			"condition": "OnBeanCondition",
			"message": "@ConditionalOnSingleCandidate (types: javax.sql.DataSource; SearchStrategy: all) found a primary bean from beans 'dataSource'"
		}],
		"DataSourceTransactionManagerAutoConfiguration.TransactionManagementConfiguration": [{
			"condition": "OnBeanCondition",
			"message": "@ConditionalOnMissingBean (types: org.springframework.transaction.annotation.AbstractTransactionManagementConfiguration; SearchStrategy: all) did not find any beans"
		}],
		"JdbcTemplateAutoConfiguration": [{
			"condition": "OnClassCondition",
			"message": "@ConditionalOnClass found required classes 'javax.sql.DataSource', 'org.springframework.jdbc.core.JdbcTemplate'"
		},
		{
			"condition": "OnBeanCondition",
			"message": "@ConditionalOnSingleCandidate (types: javax.sql.DataSource; SearchStrategy: all) found a primary bean from beans 'dataSource'"
		}],
		"JdbcTemplateAutoConfiguration#jdbcTemplate": [{
			"condition": "OnBeanCondition",
			"message": "@ConditionalOnMissingBean (types: org.springframework.jdbc.core.JdbcOperations; SearchStrategy: all) did not find any beans"
		}],
		"JdbcTemplateAutoConfiguration#namedParameterJdbcTemplate": [{
			"condition": "OnBeanCondition",
			"message": "@ConditionalOnMissingBean (types: org.springframework.jdbc.core.namedparam.NamedParameterJdbcOperations; SearchStrategy: all) did not find any beans"
		}],
		"DataSourcePoolMetadataProvidersConfiguration.TomcatDataSourcePoolMetadataProviderConfiguration": [{
			"condition": "OnClassCondition",
			"message": "@ConditionalOnClass found required class 'org.apache.tomcat.jdbc.pool.DataSource'"
		}],
		"JmxAutoConfiguration": [{
			"condition": "OnClassCondition",
			"message": "@ConditionalOnClass found required class 'org.springframework.jmx.export.MBeanExporter'"
		},
		{
			"condition": "OnPropertyCondition",
			"message": "@ConditionalOnProperty (spring.jmx.enabled=true) matched"
		}],
		"JmxAutoConfiguration#mbeanExporter": [{
			"condition": "OnBeanCondition",
			"message": "@ConditionalOnMissingBean (types: org.springframework.jmx.export.MBeanExporter; SearchStrategy: current) did not find any beans"
		}],
		"JmxAutoConfiguration#mbeanServer": [{
			"condition": "OnBeanCondition",
			"message": "@ConditionalOnMissingBean (types: javax.management.MBeanServer; SearchStrategy: all) did not find any beans"
		}],
		"JmxAutoConfiguration#objectNamingStrategy": [{
			"condition": "OnBeanCondition",
			"message": "@ConditionalOnMissingBean (types: org.springframework.jmx.export.naming.ObjectNamingStrategy; SearchStrategy: current) did not find any beans"
		}],
		"HibernateJpaAutoConfiguration": [{
			"condition": "OnClassCondition",
			"message": "@ConditionalOnClass found required classes 'org.springframework.orm.jpa.LocalContainerEntityManagerFactoryBean', 'org.springframework.transaction.annotation.EnableTransactionManagement', 'javax.persistence.EntityManager'"
		},
		{
			"condition": "HibernateJpaAutoConfiguration.HibernateEntityManagerCondition",
			"message": "HibernateEntityManager found class 'org.hibernate.ejb.HibernateEntityManager'"
		}],
		"JpaBaseConfiguration#entityManagerFactory": [{
			"condition": "OnBeanCondition",
			"message": "@ConditionalOnMissingBean (types: org.springframework.orm.jpa.LocalContainerEntityManagerFactoryBean,javax.persistence.EntityManagerFactory; SearchStrategy: all) did not find any beans"
		}],
		"JpaBaseConfiguration#entityManagerFactoryBuilder": [{
			"condition": "OnBeanCondition",
			"message": "@ConditionalOnMissingBean (types: org.springframework.boot.orm.jpa.EntityManagerFactoryBuilder; SearchStrategy: all) did not find any beans"
		}],
		"JpaBaseConfiguration#jpaVendorAdapter": [{
			"condition": "OnBeanCondition",
			"message": "@ConditionalOnMissingBean (types: org.springframework.orm.jpa.JpaVendorAdapter; SearchStrategy: all) did not find any beans"
		}],
		"JpaBaseConfiguration#transactionManager": [{
			"condition": "OnBeanCondition",
			"message": "@ConditionalOnMissingBean (types: org.springframework.transaction.PlatformTransactionManager; SearchStrategy: all) did not find any beans"
		}],
		"JpaBaseConfiguration.JpaWebConfiguration": [{
			"condition": "OnClassCondition",
			"message": "@ConditionalOnClass found required class 'org.springframework.web.servlet.config.annotation.WebMvcConfigurerAdapter'"
		},
		{
			"condition": "OnWebApplicationCondition",
			"message": "@ConditionalOnWebApplication (required) found StandardServletEnvironment"
		},
		{
			"condition": "OnPropertyCondition",
			"message": "@ConditionalOnProperty (spring.jpa.open-in-view=true) matched"
		},
		{
			"condition": "OnBeanCondition",
			"message": "@ConditionalOnMissingBean (types: org.springframework.orm.jpa.support.OpenEntityManagerInViewInterceptor,org.springframework.orm.jpa.support.OpenEntityManagerInViewFilter; SearchStrategy: all) did not find any beans"
		}],
		"TransactionAutoConfiguration": [{
			"condition": "OnClassCondition",
			"message": "@ConditionalOnClass found required classes 'org.springframework.transaction.support.TransactionTemplate', 'org.springframework.transaction.PlatformTransactionManager'"
		},
		{
			"condition": "OnBeanCondition",
			"message": "@ConditionalOnSingleCandidate (types: org.springframework.transaction.PlatformTransactionManager; SearchStrategy: all) found a primary bean from beans 'transactionManager'"
		}],
		"TransactionAutoConfiguration#transactionTemplate": [{
			"condition": "OnBeanCondition",
			"message": "@ConditionalOnMissingBean (types: org.springframework.transaction.support.TransactionTemplate; SearchStrategy: all) did not find any beans"
		}],
		"JtaAutoConfiguration": [{
			"condition": "OnClassCondition",
			"message": "@ConditionalOnClass found required class 'javax.transaction.Transaction'"
		},
		{
			"condition": "OnPropertyCondition",
			"message": "@ConditionalOnProperty (spring.jta.enabled) matched"
		}],
		"DispatcherServletAutoConfiguration": [{
			"condition": "OnClassCondition",
			"message": "@ConditionalOnClass found required class 'org.springframework.web.servlet.DispatcherServlet'"
		},
		{
			"condition": "OnWebApplicationCondition",
			"message": "@ConditionalOnWebApplication (required) found StandardServletEnvironment"
		}],
		"DispatcherServletAutoConfiguration.DispatcherServletConfiguration": [{
			"condition": "OnClassCondition",
			"message": "@ConditionalOnClass found required class 'javax.servlet.ServletRegistration'"
		},
		{
			"condition": "DispatcherServletAutoConfiguration.DefaultDispatcherServletCondition",
			"message": "Default DispatcherServlet did not find dispatcher servlet beans"
		}],
		"DispatcherServletAutoConfiguration.DispatcherServletRegistrationConfiguration": [{
			"condition": "OnClassCondition",
			"message": "@ConditionalOnClass found required class 'javax.servlet.ServletRegistration'"
		},
		{
			"condition": "DispatcherServletAutoConfiguration.DispatcherServletRegistrationCondition",
			"message": "DispatcherServlet Registration did not find servlet registration bean"
		}],
		"DispatcherServletAutoConfiguration.DispatcherServletRegistrationConfiguration#dispatcherServletRegistration": [{
			"condition": "OnBeanCondition",
			"message": "@ConditionalOnBean (names: dispatcherServlet; types: org.springframework.web.servlet.DispatcherServlet; SearchStrategy: all) found beans 'dispatcherServlet', 'dispatcherServlet'"
		}],
		"EmbeddedServletContainerAutoConfiguration": [{
			"condition": "OnWebApplicationCondition",
			"message": "@ConditionalOnWebApplication (required) found StandardServletEnvironment"
		}],
		"EmbeddedServletContainerAutoConfiguration.EmbeddedTomcat": [{
			"condition": "OnClassCondition",
			"message": "@ConditionalOnClass found required classes 'javax.servlet.Servlet', 'org.apache.catalina.startup.Tomcat'"
		},
		{
			"condition": "OnBeanCondition",
			"message": "@ConditionalOnMissingBean (types: org.springframework.boot.context.embedded.EmbeddedServletContainerFactory; SearchStrategy: current) did not find any beans"
		}],
		"ErrorMvcAutoConfiguration": [{
			"condition": "OnClassCondition",
			"message": "@ConditionalOnClass found required classes 'javax.servlet.Servlet', 'org.springframework.web.servlet.DispatcherServlet'"
		},
		{
			"condition": "OnWebApplicationCondition",
			"message": "@ConditionalOnWebApplication (required) found StandardServletEnvironment"
		}],
		"ErrorMvcAutoConfiguration#basicErrorController": [{
			"condition": "OnBeanCondition",
			"message": "@ConditionalOnMissingBean (types: org.springframework.boot.autoconfigure.web.ErrorController; SearchStrategy: current) did not find any beans"
		}],
		"ErrorMvcAutoConfiguration#conventionErrorViewResolver": [{
			"condition": "OnBeanCondition",
			"message": "@ConditionalOnBean (types: org.springframework.web.servlet.DispatcherServlet; SearchStrategy: all) found bean 'dispatcherServlet'; @ConditionalOnMissingBean (types: org.springframework.boot.autoconfigure.web.DefaultErrorViewResolver; SearchStrategy: all) did not find any beans"
		}],
		"ErrorMvcAutoConfiguration#errorAttributes": [{
			"condition": "OnBeanCondition",
			"message": "@ConditionalOnMissingBean (types: org.springframework.boot.autoconfigure.web.ErrorAttributes; SearchStrategy: current) did not find any beans"
		}],
		"ErrorMvcAutoConfiguration.WhitelabelErrorViewConfiguration": [{
			"condition": "OnPropertyCondition",
			"message": "@ConditionalOnProperty (server.error.whitelabel.enabled) matched"
		},
		{
			"condition": "ErrorMvcAutoConfiguration.ErrorTemplateMissingCondition",
			"message": "ErrorTemplate Missing did not find error template view"
		}],
		"ErrorMvcAutoConfiguration.WhitelabelErrorViewConfiguration#beanNameViewResolver": [{
			"condition": "OnBeanCondition",
			"message": "@ConditionalOnMissingBean (types: org.springframework.web.servlet.view.BeanNameViewResolver; SearchStrategy: all) did not find any beans"
		}],
		"ErrorMvcAutoConfiguration.WhitelabelErrorViewConfiguration#defaultErrorView": [{
			"condition": "OnBeanCondition",
			"message": "@ConditionalOnMissingBean (names: error; SearchStrategy: all) did not find any beans"
		}],
		"HttpEncodingAutoConfiguration": [{
			"condition": "OnClassCondition",
			"message": "@ConditionalOnClass found required class 'org.springframework.web.filter.CharacterEncodingFilter'"
		},
		{
			"condition": "OnWebApplicationCondition",
			"message": "@ConditionalOnWebApplication (required) found StandardServletEnvironment"
		},
		{
			"condition": "OnPropertyCondition",
			"message": "@ConditionalOnProperty (spring.http.encoding.enabled) matched"
		}],
		"HttpEncodingAutoConfiguration#characterEncodingFilter": [{
			"condition": "OnBeanCondition",
			"message": "@ConditionalOnMissingBean (types: org.springframework.web.filter.CharacterEncodingFilter; SearchStrategy: all) did not find any beans"
		}],
		"HttpMessageConvertersAutoConfiguration": [{
			"condition": "OnClassCondition",
			"message": "@ConditionalOnClass found required class 'org.springframework.http.converter.HttpMessageConverter'"
		}],
		"HttpMessageConvertersAutoConfiguration#messageConverters": [{
			"condition": "OnBeanCondition",
			"message": "@ConditionalOnMissingBean (types: org.springframework.boot.autoconfigure.web.HttpMessageConverters; SearchStrategy: all) did not find any beans"
		}],
		"HttpMessageConvertersAutoConfiguration.StringHttpMessageConverterConfiguration": [{
			"condition": "OnClassCondition",
			"message": "@ConditionalOnClass found required class 'org.springframework.http.converter.StringHttpMessageConverter'"
		}],
		"HttpMessageConvertersAutoConfiguration.StringHttpMessageConverterConfiguration#stringHttpMessageConverter": [{
			"condition": "OnBeanCondition",
			"message": "@ConditionalOnMissingBean (types: org.springframework.http.converter.StringHttpMessageConverter; SearchStrategy: all) did not find any beans"
		}],
		"JacksonHttpMessageConvertersConfiguration.MappingJackson2HttpMessageConverterConfiguration": [{
			"condition": "OnClassCondition",
			"message": "@ConditionalOnClass found required class 'com.fasterxml.jackson.databind.ObjectMapper'"
		},
		{
			"condition": "OnPropertyCondition",
			"message": "@ConditionalOnProperty (spring.http.converters.preferred-json-mapper=jackson) matched"
		},
		{
			"condition": "OnBeanCondition",
			"message": "@ConditionalOnBean (types: com.fasterxml.jackson.databind.ObjectMapper; SearchStrategy: all) found bean 'jacksonObjectMapper'"
		}],
		"JacksonHttpMessageConvertersConfiguration.MappingJackson2HttpMessageConverterConfiguration#mappingJackson2HttpMessageConverter": [{
			"condition": "OnBeanCondition",
			"message": "@ConditionalOnMissingBean (types: org.springframework.http.converter.json.MappingJackson2HttpMessageConverter; SearchStrategy: all) did not find any beans"
		}],
		"MultipartAutoConfiguration": [{
			"condition": "OnClassCondition",
			"message": "@ConditionalOnClass found required classes 'javax.servlet.Servlet', 'org.springframework.web.multipart.support.StandardServletMultipartResolver', 'javax.servlet.MultipartConfigElement'"
		},
		{
			"condition": "OnPropertyCondition",
			"message": "@ConditionalOnProperty (spring.http.multipart.enabled) matched"
		}],
		"MultipartAutoConfiguration#multipartConfigElement": [{
			"condition": "OnBeanCondition",
			"message": "@ConditionalOnMissingBean (types: javax.servlet.MultipartConfigElement; SearchStrategy: all) did not find any beans"
		}],
		"MultipartAutoConfiguration#multipartResolver": [{
			"condition": "OnBeanCondition",
			"message": "@ConditionalOnMissingBean (types: org.springframework.web.multipart.MultipartResolver; SearchStrategy: all) did not find any beans"
		}],
		"ServerPropertiesAutoConfiguration": [{
			"condition": "OnWebApplicationCondition",
			"message": "@ConditionalOnWebApplication (required) found StandardServletEnvironment"
		}],
		"ServerPropertiesAutoConfiguration#serverProperties": [{
			"condition": "OnBeanCondition",
			"message": "@ConditionalOnMissingBean (types: org.springframework.boot.autoconfigure.web.ServerProperties; SearchStrategy: current) did not find any beans"
		}],
		"WebClientAutoConfiguration.RestTemplateConfiguration": [{
			"condition": "OnClassCondition",
			"message": "@ConditionalOnClass found required class 'org.springframework.web.client.RestTemplate'"
		}],
		"WebClientAutoConfiguration.RestTemplateConfiguration#restTemplateBuilder": [{
			"condition": "OnBeanCondition",
			"message": "@ConditionalOnMissingBean (types: org.springframework.boot.web.client.RestTemplateBuilder; SearchStrategy: all) did not find any beans"
		}],
		"WebMvcAutoConfiguration": [{
			"condition": "OnClassCondition",
			"message": "@ConditionalOnClass found required classes 'javax.servlet.Servlet', 'org.springframework.web.servlet.DispatcherServlet', 'org.springframework.web.servlet.config.annotation.WebMvcConfigurerAdapter'"
		},
		{
			"condition": "OnWebApplicationCondition",
			"message": "@ConditionalOnWebApplication (required) found StandardServletEnvironment"
		},
		{
			"condition": "OnBeanCondition",
			"message": "@ConditionalOnMissingBean (types: org.springframework.web.servlet.config.annotation.WebMvcConfigurationSupport; SearchStrategy: all) did not find any beans"
		}],
		"WebMvcAutoConfiguration#hiddenHttpMethodFilter": [{
			"condition": "OnBeanCondition",
			"message": "@ConditionalOnMissingBean (types: org.springframework.web.filter.HiddenHttpMethodFilter; SearchStrategy: all) did not find any beans"
		}],
		"WebMvcAutoConfiguration#httpPutFormContentFilter": [{
			"condition": "OnPropertyCondition",
			"message": "@ConditionalOnProperty (spring.mvc.formcontent.putfilter.enabled) matched"
		},
		{
			"condition": "OnBeanCondition",
			"message": "@ConditionalOnMissingBean (types: org.springframework.web.filter.HttpPutFormContentFilter; SearchStrategy: all) did not find any beans"
		}],
		"WebMvcAutoConfiguration.WebMvcAutoConfigurationAdapter#defaultViewResolver": [{
			"condition": "OnBeanCondition",
			"message": "@ConditionalOnMissingBean (types: org.springframework.web.servlet.view.InternalResourceViewResolver; SearchStrategy: all) did not find any beans"
		}],
		"WebMvcAutoConfiguration.WebMvcAutoConfigurationAdapter#requestContextFilter": [{
			"condition": "OnBeanCondition",
			"message": "@ConditionalOnMissingBean (types: org.springframework.web.context.request.RequestContextListener,org.springframework.web.filter.RequestContextFilter; SearchStrategy: all) did not find any beans"
		}],
		"WebMvcAutoConfiguration.WebMvcAutoConfigurationAdapter#viewResolver": [{
			"condition": "OnBeanCondition",
			"message": "@ConditionalOnBean (types: org.springframework.web.servlet.ViewResolver; SearchStrategy: all) found beans 'defaultViewResolver', 'beanNameViewResolver', 'mvcViewResolver'; @ConditionalOnMissingBean (names: viewResolver; types: org.springframework.web.servlet.view.ContentNegotiatingViewResolver; SearchStrategy: all) did not find any beans"
		}],
		"WebMvcAutoConfiguration.WebMvcAutoConfigurationAdapter.FaviconConfiguration": [{
			"condition": "OnPropertyCondition",
			"message": "@ConditionalOnProperty (spring.mvc.favicon.enabled) matched"
		}],
		"WebSocketAutoConfiguration": [{
			"condition": "OnClassCondition",
			"message": "@ConditionalOnClass found required classes 'javax.servlet.Servlet', 'javax.websocket.server.ServerContainer'"
		},
		{
			"condition": "OnWebApplicationCondition",
			"message": "@ConditionalOnWebApplication (required) found StandardServletEnvironment"
		}],
		"WebSocketAutoConfiguration.TomcatWebSocketConfiguration": [{
			"condition": "OnClassCondition",
			"message": "@ConditionalOnClass found required classes 'org.apache.catalina.startup.Tomcat', 'org.apache.tomcat.websocket.server.WsSci'"
		}],
		"WebSocketAutoConfiguration.TomcatWebSocketConfiguration#websocketContainerCustomizer": [{
			"condition": "OnJavaCondition",
			"message": "@ConditionalOnJava (1.7 or newer) found 1.8"
		},
		{
			"condition": "OnBeanCondition",
			"message": "@ConditionalOnMissingBean (names: websocketContainerCustomizer; SearchStrategy: all) did not find any beans"
		}]
	},
	"negativeMatches": {
		"AuditAutoConfiguration#authenticationAuditListener": [{
			"condition": "OnClassCondition",
			"message": "@ConditionalOnClass did not find required class 'org.springframework.security.authentication.event.AbstractAuthenticationEvent'"
		}],
		"AuditAutoConfiguration#authorizationAuditListener": [{
			"condition": "OnClassCondition",
			"message": "@ConditionalOnClass did not find required class 'org.springframework.security.access.event.AbstractAuthorizationEvent'"
		}],
		"CacheStatisticsAutoConfiguration": [{
			"condition": "OnBeanCondition",
			"message": "@ConditionalOnBean (types: org.springframework.cache.CacheManager; SearchStrategy: all) did not find any beans"
		}],
		"CacheStatisticsAutoConfiguration.CaffeineCacheStatisticsProviderConfiguration": [{
			"condition": "OnClassCondition",
			"message": "@ConditionalOnClass did not find required classes 'com.github.benmanes.caffeine.cache.Caffeine', 'org.springframework.cache.caffeine.CaffeineCacheManager'"
		},
		{
			"condition": "ConditionEvaluationReport.AncestorsMatchedCondition",
			"message": "Ancestor org.springframework.boot.actuate.autoconfigure.CacheStatisticsAutoConfiguration did not match"
		}],
		"CacheStatisticsAutoConfiguration.ConcurrentMapCacheStatisticsConfiguration": [{
			"condition": "OnClassCondition",
			"message": "@ConditionalOnClass found required class 'org.springframework.cache.concurrent.ConcurrentMapCache'"
		},
		{
			"condition": "ConditionEvaluationReport.AncestorsMatchedCondition",
			"message": "Ancestor org.springframework.boot.actuate.autoconfigure.CacheStatisticsAutoConfiguration did not match"
		}],
		"CacheStatisticsAutoConfiguration.EhCacheCacheStatisticsProviderConfiguration": [{
			"condition": "OnClassCondition",
			"message": "@ConditionalOnClass did not find required classes 'org.springframework.cache.ehcache.EhCacheCache', 'net.sf.ehcache.Ehcache', 'net.sf.ehcache.statistics.StatisticsGateway'"
		},
		{
			"condition": "ConditionEvaluationReport.AncestorsMatchedCondition",
			"message": "Ancestor org.springframework.boot.actuate.autoconfigure.CacheStatisticsAutoConfiguration did not match"
		}],
		"CacheStatisticsAutoConfiguration.GuavaCacheStatisticsConfiguration": [{
			"condition": "OnClassCondition",
			"message": "@ConditionalOnClass did not find required classes 'com.google.common.cache.Cache', 'org.springframework.cache.guava.GuavaCache'"
		},
		{
			"condition": "ConditionEvaluationReport.AncestorsMatchedCondition",
			"message": "Ancestor org.springframework.boot.actuate.autoconfigure.CacheStatisticsAutoConfiguration did not match"
		}],
		"CacheStatisticsAutoConfiguration.HazelcastCacheStatisticsConfiguration": [{
			"condition": "OnClassCondition",
			"message": "@ConditionalOnClass did not find required classes 'com.hazelcast.core.IMap', 'com.hazelcast.spring.cache.HazelcastCache'"
		},
		{
			"condition": "ConditionEvaluationReport.AncestorsMatchedCondition",
			"message": "Ancestor org.springframework.boot.actuate.autoconfigure.CacheStatisticsAutoConfiguration did not match"
		}],
		"CacheStatisticsAutoConfiguration.InfinispanCacheStatisticsProviderConfiguration": [{
			"condition": "OnClassCondition",
			"message": "@ConditionalOnClass did not find required class 'org.infinispan.spring.provider.SpringCache'"
		},
		{
			"condition": "ConditionEvaluationReport.AncestorsMatchedCondition",
			"message": "Ancestor org.springframework.boot.actuate.autoconfigure.CacheStatisticsAutoConfiguration did not match"
		}],
		"CacheStatisticsAutoConfiguration.JCacheCacheStatisticsProviderConfiguration": [{
			"condition": "OnClassCondition",
			"message": "@ConditionalOnClass did not find required classes 'javax.cache.Caching', 'org.springframework.cache.jcache.JCacheCache'"
		},
		{
			"condition": "ConditionEvaluationReport.AncestorsMatchedCondition",
			"message": "Ancestor org.springframework.boot.actuate.autoconfigure.CacheStatisticsAutoConfiguration did not match"
		}],
		"CacheStatisticsAutoConfiguration.NoOpCacheStatisticsConfiguration": [{
			"condition": "OnClassCondition",
			"message": "@ConditionalOnClass found required class 'org.springframework.cache.support.NoOpCacheManager'"
		},
		{
			"condition": "ConditionEvaluationReport.AncestorsMatchedCondition",
			"message": "Ancestor org.springframework.boot.actuate.autoconfigure.CacheStatisticsAutoConfiguration did not match"
		}],
		"CrshAutoConfiguration": [{
			"condition": "OnClassCondition",
			"message": "@ConditionalOnClass did not find required class 'org.crsh.plugin.PluginLifeCycle'"
		}],
		"ElasticsearchHealthIndicatorConfiguration.ElasticsearchClientHealthIndicatorConfiguration": [{
			"condition": "OnEnabledHealthIndicatorCondition",
			"message": "@ConditionalOnEnabledHealthIndicator management.health.defaults.enabled is considered true"
		},
		{
			"condition": "OnBeanCondition",
			"message": "@ConditionalOnBean (types: org.elasticsearch.client.Client; SearchStrategy: all) did not find any beans"
		}],
		"ElasticsearchHealthIndicatorConfiguration.ElasticsearchJestHealthIndicatorConfiguration": [{
			"condition": "OnEnabledHealthIndicatorCondition",
			"message": "@ConditionalOnEnabledHealthIndicator management.health.defaults.enabled is considered true"
		},
		{
			"condition": "OnBeanCondition",
			"message": "@ConditionalOnBean (types: io.searchbox.client.JestClient; SearchStrategy: all) did not find any beans"
		}],
		"EndpointAutoConfiguration.FlywayEndpointConfiguration": [{
			"condition": "OnClassCondition",
			"message": "@ConditionalOnClass did not find required class 'org.flywaydb.core.Flyway'"
		}],
		"EndpointAutoConfiguration.LiquibaseEndpointConfiguration": [{
			"condition": "OnClassCondition",
			"message": "@ConditionalOnClass did not find required class 'liquibase.integration.spring.SpringLiquibase'"
		}],
		"EndpointMBeanExportAutoConfiguration#mbeanServer": [{
			"condition": "OnBeanCondition",
			"message": "@ConditionalOnMissingBean (types: javax.management.MBeanServer; SearchStrategy: all) found bean 'mbeanServer'"
		}],
		"EndpointWebMvcHypermediaManagementContextConfiguration": [{
			"condition": "OnClassCondition",
			"message": "@ConditionalOnClass did not find required class 'org.springframework.hateoas.Link'"
		}],
		"EndpointWebMvcManagementContextConfiguration#logfileMvcEndpoint": [{
			"condition": "EndpointWebMvcManagementContextConfiguration.LogFileCondition",
			"message": "Log File did not find logging file"
		}],
		"EndpointWebMvcManagementContextConfiguration#shutdownMvcEndpoint": [{
			"condition": "OnBeanCondition",
			"message": "@ConditionalOnBean (types: org.springframework.boot.actuate.endpoint.ShutdownEndpoint; SearchStrategy: all) found bean 'shutdownEndpoint'"
		},
		{
			"condition": "OnEnabledEndpointCondition",
			"message": "@ConditionalOnEnabledEndpoint (shutdown) disabled"
		}],
		"HealthIndicatorAutoConfiguration#applicationHealthIndicator": [{
			"condition": "OnBeanCondition",
			"message": "@ConditionalOnMissingBean (types: org.springframework.boot.actuate.health.HealthIndicator; SearchStrategy: all) found beans 'diskSpaceHealthIndicator', 'dbHealthIndicator'"
		}],
		"HealthIndicatorAutoConfiguration.CassandraHealthIndicatorConfiguration": [{
			"condition": "OnClassCondition",
			"message": "@ConditionalOnClass did not find required classes 'org.springframework.data.cassandra.core.CassandraOperations', 'com.datastax.driver.core.Cluster'"
		}],
		"HealthIndicatorAutoConfiguration.CouchbaseHealthIndicatorConfiguration": [{
			"condition": "OnClassCondition",
			"message": "@ConditionalOnClass did not find required classes 'org.springframework.data.couchbase.core.CouchbaseOperations', 'com.couchbase.client.java.Bucket'"
		}],
		"HealthIndicatorAutoConfiguration.JmsHealthIndicatorConfiguration": [{
			"condition": "OnEnabledHealthIndicatorCondition",
			"message": "@ConditionalOnEnabledHealthIndicator management.health.defaults.enabled is considered true"
		},
		{
			"condition": "OnBeanCondition",
			"message": "@ConditionalOnBean (types: javax.jms.ConnectionFactory; SearchStrategy: all) did not find any beans"
		}],
		"HealthIndicatorAutoConfiguration.MailHealthIndicatorConfiguration": [{
			"condition": "OnEnabledHealthIndicatorCondition",
			"message": "@ConditionalOnEnabledHealthIndicator management.health.defaults.enabled is considered true"
		},
		{
			"condition": "OnBeanCondition",
			"message": "@ConditionalOnBean (types: org.springframework.mail.javamail.JavaMailSenderImpl; SearchStrategy: all) did not find any beans"
		}],
		"HealthIndicatorAutoConfiguration.MongoHealthIndicatorConfiguration": [{
			"condition": "OnEnabledHealthIndicatorCondition",
			"message": "@ConditionalOnEnabledHealthIndicator management.health.defaults.enabled is considered true"
		},
		{
			"condition": "OnBeanCondition",
			"message": "@ConditionalOnBean (types: org.springframework.data.mongodb.core.MongoTemplate; SearchStrategy: all) did not find any beans"
		}],
		"HealthIndicatorAutoConfiguration.RabbitHealthIndicatorConfiguration": [{
			"condition": "OnEnabledHealthIndicatorCondition",
			"message": "@ConditionalOnEnabledHealthIndicator management.health.defaults.enabled is considered true"
		},
		{
			"condition": "OnBeanCondition",
			"message": "@ConditionalOnBean (types: org.springframework.amqp.rabbit.core.RabbitTemplate; SearchStrategy: all) did not find any beans"
		}],
		"HealthIndicatorAutoConfiguration.RedisHealthIndicatorConfiguration": [{
			"condition": "OnEnabledHealthIndicatorCondition",
			"message": "@ConditionalOnEnabledHealthIndicator management.health.defaults.enabled is considered true"
		},
		{
			"condition": "OnBeanCondition",
			"message": "@ConditionalOnBean (types: org.springframework.data.redis.connection.RedisConnectionFactory; SearchStrategy: all) did not find any beans"
		}],
		"HealthIndicatorAutoConfiguration.SolrHealthIndicatorConfiguration": [{
			"condition": "OnEnabledHealthIndicatorCondition",
			"message": "@ConditionalOnEnabledHealthIndicator management.health.defaults.enabled is considered true"
		},
		{
			"condition": "OnBeanCondition",
			"message": "@ConditionalOnBean (types: org.apache.solr.client.solrj.SolrClient; SearchStrategy: all) did not find any beans"
		}],
		"InfoContributorAutoConfiguration#buildInfoContributor": [{
			"condition": "OnEnabledInfoContributorCondition",
			"message": "@ConditionalOnEnabledInfoContributor management.info.defaults.enabled is considered true"
		},
		{
			"condition": "OnBeanCondition",
			"message": "@ConditionalOnSingleCandidate (types: org.springframework.boot.info.BuildProperties; SearchStrategy: all) did not find any beans"
		}],
		"InfoContributorAutoConfiguration#gitInfoContributor": [{
			"condition": "OnEnabledInfoContributorCondition",
			"message": "@ConditionalOnEnabledInfoContributor management.info.defaults.enabled is considered true"
		},
		{
			"condition": "OnBeanCondition",
			"message": "@ConditionalOnSingleCandidate (types: org.springframework.boot.info.GitProperties; SearchStrategy: all) did not find any beans"
		}],
		"JolokiaAutoConfiguration": [{
			"condition": "OnClassCondition",
			"message": "@ConditionalOnClass did not find required class 'org.jolokia.http.AgentServlet'"
		}],
		"ManagementServerPropertiesAutoConfiguration#securityProperties": [{
			"condition": "OnClassCondition",
			"message": "@ConditionalOnClass did not find required class 'org.springframework.security.config.annotation.web.configuration.EnableWebSecurity'"
		}],
		"ManagementServerPropertiesAutoConfiguration#serverProperties": [{
			"condition": "OnWebApplicationCondition",
			"message": "@ConditionalOnWebApplication (required) found StandardServletEnvironment"
		},
		{
			"condition": "OnBeanCondition",
			"message": "@ConditionalOnMissingBean (types: org.springframework.boot.autoconfigure.web.ServerProperties; SearchStrategy: all) found bean 'serverProperties'"
		}],
		"ManagementWebSecurityAutoConfiguration": [{
			"condition": "OnClassCondition",
			"message": "@ConditionalOnClass did not find required class 'org.springframework.security.config.annotation.web.configuration.EnableWebSecurity'"
		}],
		"MetricExportAutoConfiguration.StatsdConfiguration#statsdMetricWriter": [{
			"condition": "OnPropertyCondition",
			"message": "@ConditionalOnProperty (spring.metrics.export.statsd.host) did not find property 'host'"
		}],
		"MetricRepositoryAutoConfiguration.LegacyMetricRepositoryConfiguration": [{
			"condition": "OnJavaCondition",
			"message": "@ConditionalOnJava (older than 1.8) found 1.8"
		}],
		"MetricRepositoryAutoConfiguration.LegacyMetricServicesConfiguration": [{
			"condition": "OnJavaCondition",
			"message": "@ConditionalOnJava (older than 1.8) found 1.8"
		}],
		"MetricsChannelAutoConfiguration": [{
			"condition": "OnClassCondition",
			"message": "@ConditionalOnClass did not find required class 'org.springframework.messaging.MessageChannel'"
		}],
		"MetricsDropwizardAutoConfiguration": [{
			"condition": "OnClassCondition",
			"message": "@ConditionalOnClass did not find required class 'com.codahale.metrics.MetricRegistry'"
		}],
		"PublicMetricsAutoConfiguration#richGaugePublicMetrics": [{
			"condition": "OnBeanCondition",
			"message": "@ConditionalOnBean (types: org.springframework.boot.actuate.metrics.rich.RichGaugeReader; SearchStrategy: all) did not find any beans"
		}],
		"PublicMetricsAutoConfiguration.CacheStatisticsConfiguration": [{
			"condition": "OnClassCondition",
			"message": "@ConditionalOnClass found required class 'org.springframework.cache.CacheManager'"
		},
		{
			"condition": "OnBeanCondition",
			"message": "@ConditionalOnBean (types: org.springframework.cache.CacheManager; SearchStrategy: all) did not find any beans"
		}],
		"PublicMetricsAutoConfiguration.IntegrationMetricsConfiguration": [{
			"condition": "OnClassCondition",
			"message": "@ConditionalOnClass did not find required class 'org.springframework.integration.monitor.IntegrationMBeanExporter'"
		}],
		"MessageSourceAutoConfiguration": [{
			"condition": "MessageSourceAutoConfiguration.ResourceBundleCondition",
			"message": "ResourceBundle did not find bundle with basename messages"
		}],
		"SpringApplicationAdminJmxAutoConfiguration": [{
			"condition": "OnPropertyCondition",
			"message": "@ConditionalOnProperty (spring.application.admin.enabled=true) did not find property 'enabled'"
		}],
		"RabbitAutoConfiguration": [{
			"condition": "OnClassCondition",
			"message": "@ConditionalOnClass did not find required classes 'org.springframework.amqp.rabbit.core.RabbitTemplate', 'com.rabbitmq.client.Channel'"
		}],
		"AopAutoConfiguration.CglibAutoProxyConfiguration": [{
			"condition": "OnPropertyCondition",
			"message": "@ConditionalOnProperty (spring.aop.proxy-target-class=true) did not find property 'proxy-target-class'"
		}],
		"BatchAutoConfiguration": [{
			"condition": "OnClassCondition",
			"message": "@ConditionalOnClass did not find required class 'org.springframework.batch.core.launch.JobLauncher'"
		}],
		"CacheAutoConfiguration": [{
			"condition": "OnClassCondition",
			"message": "@ConditionalOnClass found required class 'org.springframework.cache.CacheManager'"
		},
		{
			"condition": "OnBeanCondition",
			"message": "@ConditionalOnBean (types: org.springframework.cache.interceptor.CacheAspectSupport; SearchStrategy: all) did not find any beans"
		}],
		"CacheAutoConfiguration.CacheManagerJpaDependencyConfiguration": [{
			"condition": "OnClassCondition",
			"message": "@ConditionalOnClass found required class 'org.springframework.orm.jpa.LocalContainerEntityManagerFactoryBean'"
		},
		{
			"condition": "ConditionEvaluationReport.AncestorsMatchedCondition",
			"message": "Ancestor org.springframework.boot.autoconfigure.cache.CacheAutoConfiguration did not match"
		}],
		"CaffeineCacheConfiguration": [{
			"condition": "OnClassCondition",
			"message": "@ConditionalOnClass did not find required classes 'com.github.benmanes.caffeine.cache.Caffeine', 'org.springframework.cache.caffeine.CaffeineCacheManager'"
		}],
		"CouchbaseCacheConfiguration": [{
			"condition": "OnClassCondition",
			"message": "@ConditionalOnClass did not find required classes 'com.couchbase.client.java.Bucket', 'com.couchbase.client.spring.cache.CouchbaseCacheManager'"
		}],
		"EhCacheCacheConfiguration": [{
			"condition": "OnClassCondition",
			"message": "@ConditionalOnClass did not find required classes 'net.sf.ehcache.Cache', 'org.springframework.cache.ehcache.EhCacheCacheManager'"
		}],
		"GuavaCacheConfiguration": [{
			"condition": "OnClassCondition",
			"message": "@ConditionalOnClass did not find required classes 'com.google.common.cache.CacheBuilder', 'org.springframework.cache.guava.GuavaCacheManager'"
		}],
		"HazelcastCacheConfiguration": [{
			"condition": "OnClassCondition",
			"message": "@ConditionalOnClass did not find required classes 'com.hazelcast.core.HazelcastInstance', 'com.hazelcast.spring.cache.HazelcastCacheManager'"
		}],
		"InfinispanCacheConfiguration": [{
			"condition": "OnClassCondition",
			"message": "@ConditionalOnClass did not find required class 'org.infinispan.spring.provider.SpringEmbeddedCacheManager'"
		}],
		"JCacheCacheConfiguration": [{
			"condition": "OnClassCondition",
			"message": "@ConditionalOnClass did not find required classes 'javax.cache.Caching', 'org.springframework.cache.jcache.JCacheCacheManager'"
		}],
		"CassandraAutoConfiguration": [{
			"condition": "OnClassCondition",
			"message": "@ConditionalOnClass did not find required class 'com.datastax.driver.core.Cluster'"
		}],
		"CloudAutoConfiguration": [{
			"condition": "OnClassCondition",
			"message": "@ConditionalOnClass did not find required class 'org.springframework.cloud.config.java.CloudScanConfiguration'"
		}],
		"CouchbaseAutoConfiguration": [{
			"condition": "OnClassCondition",
			"message": "@ConditionalOnClass did not find required classes 'com.couchbase.client.java.CouchbaseBucket', 'com.couchbase.client.java.Cluster'"
		}],
		"CassandraDataAutoConfiguration": [{
			"condition": "OnClassCondition",
			"message": "@ConditionalOnClass did not find required classes 'com.datastax.driver.core.Cluster', 'org.springframework.data.cassandra.core.CassandraAdminOperations'"
		}],
		"CassandraRepositoriesAutoConfiguration": [{
			"condition": "OnClassCondition",
			"message": "@ConditionalOnClass did not find required classes 'com.datastax.driver.core.Session', 'org.springframework.data.cassandra.repository.CassandraRepository'"
		}],
		"CouchbaseDataAutoConfiguration": [{
			"condition": "OnClassCondition",
			"message": "@ConditionalOnClass did not find required classes 'com.couchbase.client.java.Bucket', 'org.springframework.data.couchbase.repository.CouchbaseRepository'"
		}],
		"CouchbaseRepositoriesAutoConfiguration": [{
			"condition": "OnClassCondition",
			"message": "@ConditionalOnClass did not find required classes 'com.couchbase.client.java.Bucket', 'org.springframework.data.couchbase.repository.CouchbaseRepository'"
		}],
		"ElasticsearchAutoConfiguration": [{
			"condition": "OnClassCondition",
			"message": "@ConditionalOnClass did not find required classes 'org.elasticsearch.client.Client', 'org.springframework.data.elasticsearch.client.TransportClientFactoryBean', 'org.springframework.data.elasticsearch.client.NodeClientFactoryBean'"
		}],
		"ElasticsearchDataAutoConfiguration": [{
			"condition": "OnClassCondition",
			"message": "@ConditionalOnClass did not find required classes 'org.elasticsearch.client.Client', 'org.springframework.data.elasticsearch.core.ElasticsearchTemplate'"
		}],
		"ElasticsearchRepositoriesAutoConfiguration": [{
			"condition": "OnClassCondition",
			"message": "@ConditionalOnClass did not find required classes 'org.elasticsearch.client.Client', 'org.springframework.data.elasticsearch.repository.ElasticsearchRepository'"
		}],
		"MongoDataAutoConfiguration": [{
			"condition": "OnClassCondition",
			"message": "@ConditionalOnClass did not find required classes 'com.mongodb.Mongo', 'org.springframework.data.mongodb.core.MongoTemplate'"
		}],
		"MongoRepositoriesAutoConfiguration": [{
			"condition": "OnClassCondition",
			"message": "@ConditionalOnClass did not find required classes 'com.mongodb.Mongo', 'org.springframework.data.mongodb.repository.MongoRepository'"
		}],
		"Neo4jDataAutoConfiguration": [{
			"condition": "OnClassCondition",
			"message": "@ConditionalOnClass did not find required classes 'org.neo4j.ogm.session.Neo4jSession', 'org.springframework.data.neo4j.template.Neo4jOperations'"
		}],
		"Neo4jRepositoriesAutoConfiguration": [{
			"condition": "OnClassCondition",
			"message": "@ConditionalOnClass did not find required classes 'org.neo4j.ogm.session.Neo4jSession', 'org.springframework.data.neo4j.repository.GraphRepository'"
		}],
		"RedisAutoConfiguration": [{
			"condition": "OnClassCondition",
			"message": "@ConditionalOnClass did not find required classes 'org.springframework.data.redis.connection.jedis.JedisConnection', 'org.springframework.data.redis.core.RedisOperations', 'redis.clients.jedis.Jedis'"
		}],
		"RedisRepositoriesAutoConfiguration": [{
			"condition": "OnClassCondition",
			"message": "@ConditionalOnClass did not find required classes 'redis.clients.jedis.Jedis', 'org.springframework.data.redis.repository.configuration.EnableRedisRepositories'"
		}],
		"RepositoryRestMvcAutoConfiguration": [{
			"condition": "OnClassCondition",
			"message": "@ConditionalOnClass did not find required class 'org.springframework.data.rest.webmvc.config.RepositoryRestMvcConfiguration'"
		}],
		"SolrRepositoriesAutoConfiguration": [{
			"condition": "OnClassCondition",
			"message": "@ConditionalOnClass did not find required classes 'org.apache.solr.client.solrj.SolrClient', 'org.springframework.data.solr.repository.SolrRepository'"
		}],
		"JestAutoConfiguration": [{
			"condition": "OnClassCondition",
			"message": "@ConditionalOnClass did not find required class 'io.searchbox.client.JestClient'"
		}],
		"FlywayAutoConfiguration": [{
			"condition": "OnClassCondition",
			"message": "@ConditionalOnClass did not find required class 'org.flywaydb.core.Flyway'"
		}],
		"FreeMarkerAutoConfiguration": [{
			"condition": "OnClassCondition",
			"message": "@ConditionalOnClass did not find required classes 'freemarker.template.Configuration', 'org.springframework.ui.freemarker.FreeMarkerConfigurationFactory'"
		}],
		"GroovyTemplateAutoConfiguration": [{
			"condition": "OnClassCondition",
			"message": "@ConditionalOnClass did not find required class 'groovy.text.markup.MarkupTemplateEngine'"
		}],
		"GsonAutoConfiguration": [{
			"condition": "OnClassCondition",
			"message": "@ConditionalOnClass did not find required class 'com.google.gson.Gson'"
		}],
		"H2ConsoleAutoConfiguration": [{
			"condition": "OnClassCondition",
			"message": "@ConditionalOnClass found required class 'org.h2.server.web.WebServlet'"
		},
		{
			"condition": "OnWebApplicationCondition",
			"message": "@ConditionalOnWebApplication (required) found StandardServletEnvironment"
		},
		{
			"condition": "OnPropertyCondition",
			"message": "@ConditionalOnProperty (spring.h2.console.enabled=true) did not find property 'enabled'"
		}],
		"HypermediaAutoConfiguration": [{
			"condition": "OnClassCondition",
			"message": "@ConditionalOnClass did not find required classes 'org.springframework.hateoas.Resource', 'org.springframework.plugin.core.Plugin'"
		}],
		"HazelcastAutoConfiguration": [{
			"condition": "OnClassCondition",
			"message": "@ConditionalOnClass did not find required class 'com.hazelcast.core.HazelcastInstance'"
		}],
		"HazelcastJpaDependencyAutoConfiguration": [{
			"condition": "OnClassCondition",
			"message": "@ConditionalOnClass did not find required class 'com.hazelcast.core.HazelcastInstance'"
		}],
		"ProjectInfoAutoConfiguration#buildProperties": [{
			"condition": "OnResourceCondition",
			"message": "@ConditionalOnResource did not find resource '${spring.info.build.location:classpath:META-INF/build-info.properties}'"
		}],
		"ProjectInfoAutoConfiguration#gitProperties": [{
			"condition": "ProjectInfoAutoConfiguration.GitResourceAvailableCondition",
			"message": "GitResource did not find git info at classpath:git.properties"
		}],
		"IntegrationAutoConfiguration": [{
			"condition": "OnClassCondition",
			"message": "@ConditionalOnClass did not find required class 'org.springframework.integration.config.EnableIntegration'"
		}],
		"JacksonAutoConfiguration.JodaDateTimeJacksonConfiguration": [{
			"condition": "OnClassCondition",
			"message": "@ConditionalOnClass did not find required classes 'org.joda.time.DateTime', 'com.fasterxml.jackson.datatype.joda.ser.DateTimeSerializer', 'com.fasterxml.jackson.datatype.joda.cfg.JacksonJodaDateFormat'"
		}],
		"JacksonAutoConfiguration.ParameterNamesModuleConfiguration": [{
			"condition": "OnClassCondition",
			"message": "@ConditionalOnClass did not find required class 'com.fasterxml.jackson.module.paramnames.ParameterNamesModule'"
		}],
		"DataSourceAutoConfiguration.EmbeddedDatabaseConfiguration": [{
			"condition": "DataSourceAutoConfiguration.EmbeddedDatabaseCondition",
			"message": "EmbeddedDataSource found supported pooled data source"
		}],
		"DataSourceAutoConfiguration.TomcatDataSourceJmxConfiguration": [{
			"condition": "OnClassCondition",
			"message": "@ConditionalOnClass found required class 'org.apache.tomcat.jdbc.pool.DataSourceProxy'"
		},
		{
			"condition": "OnPropertyCondition",
			"message": "@ConditionalOnProperty (spring.datasource.jmx-enabled) did not find property 'jmx-enabled'"
		}],
		"DataSourceConfiguration.Dbcp": [{
			"condition": "OnClassCondition",
			"message": "@ConditionalOnClass did not find required class 'org.apache.commons.dbcp.BasicDataSource'"
		}],
		"DataSourceConfiguration.Dbcp2": [{
			"condition": "OnClassCondition",
			"message": "@ConditionalOnClass did not find required class 'org.apache.commons.dbcp2.BasicDataSource'"
		}],
		"DataSourceConfiguration.Generic": [{
			"condition": "OnPropertyCondition",
			"message": "@ConditionalOnProperty (spring.datasource.type) did not find property 'spring.datasource.type'"
		}],
		"DataSourceConfiguration.Hikari": [{
			"condition": "OnClassCondition",
			"message": "@ConditionalOnClass did not find required class 'com.zaxxer.hikari.HikariDataSource'"
		}],
		"DataSourceTransactionManagerAutoConfiguration.DataSourceTransactionManagerConfiguration#transactionManager": [{
			"condition": "OnBeanCondition",
			"message": "@ConditionalOnMissingBean (types: org.springframework.transaction.PlatformTransactionManager; SearchStrategy: all) found bean 'transactionManager'"
		}],
		"JndiDataSourceAutoConfiguration": [{
			"condition": "OnClassCondition",
			"message": "@ConditionalOnClass found required classes 'javax.sql.DataSource', 'org.springframework.jdbc.datasource.embedded.EmbeddedDatabaseType'"
		},
		{
			"condition": "OnPropertyCondition",
			"message": "@ConditionalOnProperty (spring.datasource.jndi-name) did not find property 'jndi-name'"
		}],
		"XADataSourceAutoConfiguration": [{
			"condition": "OnClassCondition",
			"message": "@ConditionalOnClass found required classes 'javax.sql.DataSource', 'javax.transaction.TransactionManager', 'org.springframework.jdbc.datasource.embedded.EmbeddedDatabaseType'"
		},
		{
			"condition": "OnBeanCondition",
			"message": "@ConditionalOnBean (types: org.springframework.boot.jta.XADataSourceWrapper; SearchStrategy: all) did not find any beans"
		}],
		"DataSourcePoolMetadataProvidersConfiguration.CommonsDbcp2PoolDataSourceMetadataProviderConfiguration": [{
			"condition": "OnClassCondition",
			"message": "@ConditionalOnClass did not find required class 'org.apache.commons.dbcp2.BasicDataSource'"
		}],
		"DataSourcePoolMetadataProvidersConfiguration.CommonsDbcpPoolDataSourceMetadataProviderConfiguration": [{
			"condition": "OnClassCondition",
			"message": "@ConditionalOnClass did not find required class 'org.apache.commons.dbcp.BasicDataSource'"
		}],
		"DataSourcePoolMetadataProvidersConfiguration.HikariPoolDataSourceMetadataProviderConfiguration": [{
			"condition": "OnClassCondition",
			"message": "@ConditionalOnClass did not find required class 'com.zaxxer.hikari.HikariDataSource'"
		}],
		"JerseyAutoConfiguration": [{
			"condition": "OnClassCondition",
			"message": "@ConditionalOnClass did not find required class 'org.glassfish.jersey.server.spring.SpringComponentProvider'"
		}],
		"JmsAutoConfiguration": [{
			"condition": "OnClassCondition",
			"message": "@ConditionalOnClass did not find required class 'org.springframework.jms.core.JmsTemplate'"
		}],
		"JndiConnectionFactoryAutoConfiguration": [{
			"condition": "OnClassCondition",
			"message": "@ConditionalOnClass did not find required class 'org.springframework.jms.core.JmsTemplate'"
		}],
		"ActiveMQAutoConfiguration": [{
			"condition": "OnClassCondition",
			"message": "@ConditionalOnClass did not find required classes 'javax.jms.ConnectionFactory', 'org.apache.activemq.ActiveMQConnectionFactory'"
		}],
		"ArtemisAutoConfiguration": [{
			"condition": "OnClassCondition",
			"message": "@ConditionalOnClass did not find required classes 'javax.jms.ConnectionFactory', 'org.apache.activemq.artemis.jms.client.ActiveMQConnectionFactory'"
		}],
		"HornetQAutoConfiguration": [{
			"condition": "OnClassCondition",
			"message": "@ConditionalOnClass did not find required classes 'javax.jms.ConnectionFactory', 'org.hornetq.api.jms.HornetQJMSClient'"
		}],
		"JooqAutoConfiguration": [{
			"condition": "OnClassCondition",
			"message": "@ConditionalOnClass did not find required class 'org.jooq.DSLContext'"
		}],
		"LiquibaseAutoConfiguration": [{
			"condition": "OnClassCondition",
			"message": "@ConditionalOnClass did not find required class 'liquibase.integration.spring.SpringLiquibase'"
		}],
		"MailSenderAutoConfiguration": [{
			"condition": "OnClassCondition",
			"message": "@ConditionalOnClass did not find required class 'javax.mail.internet.MimeMessage'"
		}],
		"MailSenderValidatorAutoConfiguration": [{
			"condition": "OnPropertyCondition",
			"message": "@ConditionalOnProperty (spring.mail.test-connection) did not find property 'test-connection'"
		}],
		"DeviceDelegatingViewResolverAutoConfiguration": [{
			"condition": "OnClassCondition",
			"message": "@ConditionalOnClass did not find required class 'org.springframework.mobile.device.view.LiteDeviceDelegatingViewResolver'"
		}],
		"DeviceResolverAutoConfiguration": [{
			"condition": "OnClassCondition",
			"message": "@ConditionalOnClass did not find required classes 'org.springframework.mobile.device.DeviceResolverHandlerInterceptor', 'org.springframework.mobile.device.DeviceHandlerMethodArgumentResolver'"
		}],
		"SitePreferenceAutoConfiguration": [{
			"condition": "OnClassCondition",
			"message": "@ConditionalOnClass did not find required classes 'org.springframework.mobile.device.site.SitePreferenceHandlerInterceptor', 'org.springframework.mobile.device.site.SitePreferenceHandlerMethodArgumentResolver'"
		}],
		"MongoAutoConfiguration": [{
			"condition": "OnClassCondition",
			"message": "@ConditionalOnClass did not find required class 'com.mongodb.MongoClient'"
		}],
		"EmbeddedMongoAutoConfiguration": [{
			"condition": "OnClassCondition",
			"message": "@ConditionalOnClass did not find required classes 'com.mongodb.Mongo', 'de.flapdoodle.embed.mongo.MongodStarter'"
		}],
		"MustacheAutoConfiguration": [{
			"condition": "OnClassCondition",
			"message": "@ConditionalOnClass did not find required class 'com.samskivert.mustache.Mustache'"
		}],
		"ReactorAutoConfiguration": [{
			"condition": "OnClassCondition",
			"message": "@ConditionalOnClass did not find required classes 'reactor.spring.context.config.EnableReactor', 'reactor.Environment'"
		}],
		"FallbackWebSecurityAutoConfiguration": [{
			"condition": "OnClassCondition",
			"message": "@ConditionalOnClass did not find required class 'org.springframework.security.config.annotation.web.configuration.EnableWebSecurity'"
		}],
		"SecurityAutoConfiguration": [{
			"condition": "OnClassCondition",
			"message": "@ConditionalOnClass did not find required classes 'org.springframework.security.authentication.AuthenticationManager', 'org.springframework.security.config.annotation.authentication.configurers.GlobalAuthenticationConfigurerAdapter'"
		}],
		"SecurityFilterAutoConfiguration": [{
			"condition": "OnClassCondition",
			"message": "@ConditionalOnClass did not find required classes 'org.springframework.security.web.context.AbstractSecurityWebApplicationInitializer', 'org.springframework.security.config.http.SessionCreationPolicy'"
		}],
		"OAuth2AutoConfiguration": [{
			"condition": "OnClassCondition",
			"message": "@ConditionalOnClass did not find required class 'org.springframework.security.oauth2.common.OAuth2AccessToken'"
		}],
		"SendGridAutoConfiguration": [{
			"condition": "OnClassCondition",
			"message": "@ConditionalOnClass did not find required class 'com.sendgrid.SendGrid'"
		}],
		"SessionAutoConfiguration": [{
			"condition": "OnClassCondition",
			"message": "@ConditionalOnClass did not find required class 'org.springframework.session.Session'"
		}],
		"FacebookAutoConfiguration": [{
			"condition": "OnClassCondition",
			"message": "@ConditionalOnClass did not find required classes 'org.springframework.social.config.annotation.SocialConfigurerAdapter', 'org.springframework.social.facebook.connect.FacebookConnectionFactory'"
		}],
		"LinkedInAutoConfiguration": [{
			"condition": "OnClassCondition",
			"message": "@ConditionalOnClass did not find required classes 'org.springframework.social.config.annotation.SocialConfigurerAdapter', 'org.springframework.social.linkedin.connect.LinkedInConnectionFactory'"
		}],
		"SocialWebAutoConfiguration": [{
			"condition": "OnClassCondition",
			"message": "@ConditionalOnClass did not find required classes 'org.springframework.social.connect.web.ConnectController', 'org.springframework.social.config.annotation.SocialConfigurerAdapter'"
		}],
		"TwitterAutoConfiguration": [{
			"condition": "OnClassCondition",
			"message": "@ConditionalOnClass did not find required classes 'org.springframework.social.config.annotation.SocialConfigurerAdapter', 'org.springframework.social.twitter.connect.TwitterConnectionFactory'"
		}],
		"SolrAutoConfiguration": [{
			"condition": "OnClassCondition",
			"message": "@ConditionalOnClass did not find required classes 'org.apache.solr.client.solrj.impl.HttpSolrClient', 'org.apache.solr.client.solrj.impl.CloudSolrClient'"
		}],
		"ThymeleafAutoConfiguration": [{
			"condition": "OnClassCondition",
			"message": "@ConditionalOnClass did not find required class 'org.thymeleaf.spring4.SpringTemplateEngine'"
		}],
		"AtomikosJtaConfiguration": [{
			"condition": "OnClassCondition",
			"message": "@ConditionalOnClass did not find required class 'com.atomikos.icatch.jta.UserTransactionManager'"
		}],
		"BitronixJtaConfiguration": [{
			"condition": "OnClassCondition",
			"message": "@ConditionalOnClass did not find required class 'bitronix.tm.jndi.BitronixContext'"
		}],
		"JndiJtaConfiguration": [{
			"condition": "OnClassCondition",
			"message": "@ConditionalOnClass found required class 'org.springframework.transaction.jta.JtaTransactionManager'"
		},
		{
			"condition": "OnJndiCondition",
			"message": "@ConditionalOnJndi JNDI environment is not available"
		}],
		"NarayanaJtaConfiguration": [{
			"condition": "OnClassCondition",
			"message": "@ConditionalOnClass did not find required classes 'com.arjuna.ats.jta.UserTransaction', 'org.jboss.tm.XAResourceRecoveryRegistry'"
		}],
		"VelocityAutoConfiguration": [{
			"condition": "OnClassCondition",
			"message": "@ConditionalOnClass did not find required classes 'org.apache.velocity.app.VelocityEngine', 'org.springframework.ui.velocity.VelocityEngineFactory'"
		}],
		"DispatcherServletAutoConfiguration.DispatcherServletConfiguration#multipartResolver": [{
			"condition": "OnBeanCondition",
			"message": "@ConditionalOnBean (types: org.springframework.web.multipart.MultipartResolver; SearchStrategy: all) did not find any beans"
		}],
		"EmbeddedServletContainerAutoConfiguration.EmbeddedJetty": [{
			"condition": "OnClassCondition",
			"message": "@ConditionalOnClass did not find required classes 'org.eclipse.jetty.server.Server', 'org.eclipse.jetty.util.Loader', 'org.eclipse.jetty.webapp.WebAppContext'"
		}],
		"EmbeddedServletContainerAutoConfiguration.EmbeddedUndertow": [{
			"condition": "OnClassCondition",
			"message": "@ConditionalOnClass did not find required classes 'io.undertow.Undertow', 'org.xnio.SslClientAuthMode'"
		}],
		"GsonHttpMessageConvertersConfiguration": [{
			"condition": "OnClassCondition",
			"message": "@ConditionalOnClass did not find required class 'com.google.gson.Gson'"
		}],
		"JacksonHttpMessageConvertersConfiguration.MappingJackson2XmlHttpMessageConverterConfiguration": [{
			"condition": "OnClassCondition",
			"message": "@ConditionalOnClass did not find required class 'com.fasterxml.jackson.dataformat.xml.XmlMapper'"
		}],
		"WebMvcAutoConfiguration.ResourceChainCustomizerConfiguration": [{
			"condition": "OnEnabledResourceChainCondition",
			"message": "@ConditionalOnEnabledResourceChain did not find class org.webjars.WebJarAssetLocator"
		}],
		"WebMvcAutoConfiguration.WebMvcAutoConfigurationAdapter#beanNameViewResolver": [{
			"condition": "OnBeanCondition",
			"message": "@ConditionalOnMissingBean (types: org.springframework.web.servlet.view.BeanNameViewResolver; SearchStrategy: all) found bean 'beanNameViewResolver'"
		}],
		"WebMvcAutoConfiguration.WebMvcAutoConfigurationAdapter#dateFormatter": [{
			"condition": "OnPropertyCondition",
			"message": "@ConditionalOnProperty (spring.mvc.date-format) did not find property 'date-format'"
		}],
		"WebMvcAutoConfiguration.WebMvcAutoConfigurationAdapter#localeResolver": [{
			"condition": "OnPropertyCondition",
			"message": "@ConditionalOnProperty (spring.mvc.locale) did not find property 'locale'"
		}],
		"WebServicesAutoConfiguration": [{
			"condition": "OnClassCondition",
			"message": "@ConditionalOnClass did not find required class 'org.springframework.ws.transport.http.MessageDispatcherServlet'"
		}],
		"WebSocketAutoConfiguration.JettyWebSocketConfiguration": [{
			"condition": "OnClassCondition",
			"message": "@ConditionalOnClass did not find required class 'org.eclipse.jetty.websocket.jsr356.server.deploy.WebSocketServerContainerInitializer'"
		}],
		"WebSocketAutoConfiguration.UndertowWebSocketConfiguration": [{
			"condition": "OnClassCondition",
			"message": "@ConditionalOnClass did not find required class 'io.undertow.websockets.jsr.Bootstrap'"
		}],
		"WebSocketMessagingAutoConfiguration": [{
			"condition": "OnClassCondition",
			"message": "@ConditionalOnClass did not find required class 'org.springframework.web.socket.config.annotation.WebSocketMessageBrokerConfigurer'"
		}]
	}
}