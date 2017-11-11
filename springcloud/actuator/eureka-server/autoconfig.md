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
			"message": "@ConditionalOnBean (types: org.springframework.boot.actuate.metrics.CounterService,org.springframework.boot.actuate.metrics.GaugeService; SearchStrategy: all) found beans 'servoMetricServices', 'servoMetricServices'"
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
		"AopAutoConfiguration.CglibAutoProxyConfiguration": [{
			"condition": "OnPropertyCondition",
			"message": "@ConditionalOnProperty (spring.aop.proxy-target-class=true) matched"
		}],
		"GenericCacheConfiguration": [{
			"condition": "CacheCondition",
			"message": "Cache org.springframework.boot.autoconfigure.cache.GenericCacheConfiguration automatic cache type"
		}],
		"GuavaCacheConfiguration": [{
			"condition": "OnClassCondition",
			"message": "@ConditionalOnClass found required classes 'com.google.common.cache.CacheBuilder', 'org.springframework.cache.guava.GuavaCacheManager'"
		},
		{
			"condition": "CacheCondition",
			"message": "Cache org.springframework.boot.autoconfigure.cache.GuavaCacheConfiguration automatic cache type"
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
		"FreeMarkerAutoConfiguration": [{
			"condition": "OnClassCondition",
			"message": "@ConditionalOnClass found required classes 'freemarker.template.Configuration', 'org.springframework.ui.freemarker.FreeMarkerConfigurationFactory'"
		}],
		"FreeMarkerAutoConfiguration.FreeMarkerWebConfiguration": [{
			"condition": "OnClassCondition",
			"message": "@ConditionalOnClass found required class 'javax.servlet.Servlet'"
		},
		{
			"condition": "OnWebApplicationCondition",
			"message": "@ConditionalOnWebApplication (required) found StandardServletEnvironment"
		}],
		"FreeMarkerAutoConfiguration.FreeMarkerWebConfiguration#freeMarkerConfigurer": [{
			"condition": "OnBeanCondition",
			"message": "@ConditionalOnMissingBean (types: org.springframework.web.servlet.view.freemarker.FreeMarkerConfig; SearchStrategy: all) did not find any beans"
		}],
		"FreeMarkerAutoConfiguration.FreeMarkerWebConfiguration#freeMarkerViewResolver": [{
			"condition": "OnPropertyCondition",
			"message": "@ConditionalOnProperty (spring.freemarker.enabled) matched"
		},
		{
			"condition": "OnBeanCondition",
			"message": "@ConditionalOnMissingBean (names: freeMarkerViewResolver; SearchStrategy: all) did not find any beans"
		}],
		"GsonAutoConfiguration": [{
			"condition": "OnClassCondition",
			"message": "@ConditionalOnClass found required class 'com.google.gson.Gson'"
		}],
		"GsonAutoConfiguration#gson": [{
			"condition": "OnBeanCondition",
			"message": "@ConditionalOnMissingBean (types: com.google.gson.Gson; SearchStrategy: all) did not find any beans"
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
		"GsonHttpMessageConvertersConfiguration": [{
			"condition": "OnClassCondition",
			"message": "@ConditionalOnClass found required class 'com.google.gson.Gson'"
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
		"JacksonHttpMessageConvertersConfiguration.MappingJackson2XmlHttpMessageConverterConfiguration": [{
			"condition": "OnClassCondition",
			"message": "@ConditionalOnClass found required class 'com.fasterxml.jackson.dataformat.xml.XmlMapper'"
		},
		{
			"condition": "OnBeanCondition",
			"message": "@ConditionalOnBean (types: org.springframework.http.converter.json.Jackson2ObjectMapperBuilder; SearchStrategy: all) found bean 'jacksonObjectMapperBuilder'"
		}],
		"JacksonHttpMessageConvertersConfiguration.MappingJackson2XmlHttpMessageConverterConfiguration#mappingJackson2XmlHttpMessageConverter": [{
			"condition": "OnBeanCondition",
			"message": "@ConditionalOnMissingBean (types: org.springframework.http.converter.xml.MappingJackson2XmlHttpMessageConverter; SearchStrategy: all) did not find any beans"
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
		}],
		"ConfigurationPropertiesRebinderAutoConfiguration": [{
			"condition": "OnBeanCondition",
			"message": "@ConditionalOnBean (types: org.springframework.boot.context.properties.ConfigurationPropertiesBindingPostProcessor; SearchStrategy: all) found bean 'org.springframework.boot.context.properties.ConfigurationPropertiesBindingPostProcessor'"
		}],
		"ConfigurationPropertiesRebinderAutoConfiguration#configurationPropertiesBeans": [{
			"condition": "OnBeanCondition",
			"message": "@ConditionalOnMissingBean (types: org.springframework.cloud.context.properties.ConfigurationPropertiesBeans; SearchStrategy: current) did not find any beans"
		}],
		"ConfigurationPropertiesRebinderAutoConfiguration#configurationPropertiesRebinder": [{
			"condition": "OnBeanCondition",
			"message": "@ConditionalOnMissingBean (types: org.springframework.cloud.context.properties.ConfigurationPropertiesRebinder; SearchStrategy: current) did not find any beans"
		}],
		"LifecycleMvcEndpointAutoConfiguration": [{
			"condition": "OnClassCondition",
			"message": "@ConditionalOnClass found required class 'org.springframework.boot.actuate.endpoint.EnvironmentEndpoint'"
		},
		{
			"condition": "OnWebApplicationCondition",
			"message": "@ConditionalOnWebApplication (required) found StandardServletEnvironment"
		},
		{
			"condition": "OnBeanCondition",
			"message": "@ConditionalOnBean (types: org.springframework.cloud.context.restart.RestartEndpoint; SearchStrategy: all) found bean 'restartEndpoint'"
		}],
		"LifecycleMvcEndpointAutoConfiguration#environmentManagerEndpoint": [{
			"condition": "OnPropertyCondition",
			"message": "@ConditionalOnProperty (endpoints.env.post.enabled) matched"
		},
		{
			"condition": "OnBeanCondition",
			"message": "@ConditionalOnBean (types: org.springframework.boot.actuate.endpoint.EnvironmentEndpoint; SearchStrategy: all) found bean 'environmentEndpoint'"
		}],
		"LifecycleMvcEndpointAutoConfiguration#pauseMvcEndpoint": [{
			"condition": "OnBeanCondition",
			"message": "@ConditionalOnBean (types: org.springframework.cloud.context.restart.RestartEndpoint$PauseEndpoint; SearchStrategy: all) found bean 'pauseEndpoint'"
		}],
		"LifecycleMvcEndpointAutoConfiguration#refreshMvcEndpoint": [{
			"condition": "OnBeanCondition",
			"message": "@ConditionalOnBean (types: org.springframework.cloud.endpoint.RefreshEndpoint; SearchStrategy: all) found bean 'refreshEndpoint'"
		}],
		"LifecycleMvcEndpointAutoConfiguration#resumeMvcEndpoint": [{
			"condition": "OnBeanCondition",
			"message": "@ConditionalOnBean (types: org.springframework.cloud.context.restart.RestartEndpoint$ResumeEndpoint; SearchStrategy: all) found bean 'resumeEndpoint'"
		}],
		"RefreshAutoConfiguration": [{
			"condition": "OnClassCondition",
			"message": "@ConditionalOnClass found required class 'org.springframework.cloud.context.scope.refresh.RefreshScope'"
		}],
		"RefreshAutoConfiguration#contextRefresher": [{
			"condition": "OnBeanCondition",
			"message": "@ConditionalOnMissingBean (types: org.springframework.cloud.context.refresh.ContextRefresher; SearchStrategy: all) did not find any beans"
		}],
		"RefreshAutoConfiguration#environmentManager": [{
			"condition": "OnBeanCondition",
			"message": "@ConditionalOnMissingBean (types: org.springframework.cloud.context.environment.EnvironmentManager; SearchStrategy: all) did not find any beans"
		}],
		"RefreshAutoConfiguration#loggingRebinder": [{
			"condition": "OnBeanCondition",
			"message": "@ConditionalOnMissingBean (types: org.springframework.cloud.logging.LoggingRebinder; SearchStrategy: all) did not find any beans"
		}],
		"RefreshAutoConfiguration#refreshScope": [{
			"condition": "OnBeanCondition",
			"message": "@ConditionalOnMissingBean (types: org.springframework.cloud.context.scope.refresh.RefreshScope; SearchStrategy: all) did not find any beans"
		}],
		"RefreshEndpointAutoConfiguration": [{
			"condition": "OnClassCondition",
			"message": "@ConditionalOnClass found required class 'org.springframework.boot.actuate.endpoint.Endpoint'"
		}],
		"RefreshEndpointAutoConfiguration#refreshScopeHealthIndicator": [{
			"condition": "OnBeanCondition",
			"message": "@ConditionalOnMissingBean (types: org.springframework.cloud.health.RefreshScopeHealthIndicator; SearchStrategy: all) did not find any beans"
		},
		{
			"condition": "OnEnabledHealthIndicatorCondition",
			"message": "@ConditionalOnEnabledHealthIndicator management.health.defaults.enabled is considered true"
		}],
		"RefreshEndpointAutoConfiguration.RefreshEndpointConfiguration": [{
			"condition": "OnPropertyCondition",
			"message": "@ConditionalOnProperty (endpoints.refresh.enabled) matched"
		},
		{
			"condition": "OnBeanCondition",
			"message": "@ConditionalOnBean (types: org.springframework.cloud.bootstrap.config.PropertySourceBootstrapConfiguration; SearchStrategy: all) found bean 'propertySourceBootstrapConfiguration'"
		}],
		"RefreshEndpointAutoConfiguration.RefreshEndpointConfiguration#refreshEndpoint": [{
			"condition": "OnBeanCondition",
			"message": "@ConditionalOnMissingBean (types: org.springframework.cloud.endpoint.RefreshEndpoint; SearchStrategy: all) did not find any beans"
		}],
		"RefreshEndpointAutoConfiguration.RestartEndpointWithoutIntegration": [{
			"condition": "OnClassCondition",
			"message": "@ConditionalOnMissingClass did not find unwanted class 'org.springframework.integration.monitor.IntegrationMBeanExporter'"
		}],
		"RefreshEndpointAutoConfiguration.RestartEndpointWithoutIntegration#restartEndpoint": [{
			"condition": "OnBeanCondition",
			"message": "@ConditionalOnMissingBean (types: org.springframework.cloud.context.restart.RestartEndpoint; SearchStrategy: all) did not find any beans"
		}],
		"CommonsClientAutoConfiguration": [{
			"condition": "OnClassCondition",
			"message": "@ConditionalOnClass found required class 'org.springframework.boot.actuate.health.HealthIndicator'"
		},
		{
			"condition": "OnPropertyCondition",
			"message": "@ConditionalOnProperty (spring.cloud.discovery.enabled) matched"
		},
		{
			"condition": "OnBeanCondition",
			"message": "@ConditionalOnBean (types: org.springframework.cloud.client.discovery.DiscoveryClient; SearchStrategy: all) found bean 'discoveryClient'"
		}],
		"CommonsClientAutoConfiguration#discoveryClientHealthIndicator": [{
			"condition": "OnPropertyCondition",
			"message": "@ConditionalOnProperty (spring.cloud.discovery.client.health-indicator.enabled) matched"
		}],
		"CommonsClientAutoConfiguration#discoveryCompositeHealthIndicator": [{
			"condition": "OnPropertyCondition",
			"message": "@ConditionalOnProperty (spring.cloud.discovery.client.composite-indicator.enabled) matched"
		},
		{
			"condition": "OnBeanCondition",
			"message": "@ConditionalOnBean (types: org.springframework.cloud.client.discovery.health.DiscoveryHealthIndicator; SearchStrategy: all) found beans 'discoveryClientHealthIndicator', 'eurekaHealthIndicator'"
		}],
		"CommonsClientAutoConfiguration.ActuatorConfiguration": [{
			"condition": "OnClassCondition",
			"message": "@ConditionalOnClass found required class 'org.springframework.boot.actuate.endpoint.Endpoint'"
		},
		{
			"condition": "OnPropertyCondition",
			"message": "@ConditionalOnProperty (spring.cloud.features.enabled) matched"
		}],
		"LoadBalancerAutoConfiguration": [{
			"condition": "OnClassCondition",
			"message": "@ConditionalOnClass found required class 'org.springframework.web.client.RestTemplate'"
		},
		{
			"condition": "OnBeanCondition",
			"message": "@ConditionalOnBean (types: org.springframework.cloud.client.loadbalancer.LoadBalancerClient; SearchStrategy: all) found bean 'loadBalancerClient'"
		}],
		"LoadBalancerAutoConfiguration#loadBalancerRequestFactory": [{
			"condition": "OnBeanCondition",
			"message": "@ConditionalOnMissingBean (types: org.springframework.cloud.client.loadbalancer.LoadBalancerRequestFactory; SearchStrategy: all) did not find any beans"
		}],
		"LoadBalancerAutoConfiguration.RetryAutoConfiguration": [{
			"condition": "OnClassCondition",
			"message": "@ConditionalOnClass found required class 'org.springframework.retry.support.RetryTemplate'"
		}],
		"LoadBalancerAutoConfiguration.RetryAutoConfiguration#restTemplateCustomizer": [{
			"condition": "OnBeanCondition",
			"message": "@ConditionalOnMissingBean (types: org.springframework.cloud.client.loadbalancer.RestTemplateCustomizer; SearchStrategy: all) did not find any beans"
		}],
		"UtilAutoConfiguration": [{
			"condition": "OnPropertyCondition",
			"message": "@ConditionalOnProperty (spring.cloud.util.enabled) matched"
		}],
		"UtilAutoConfiguration#inetUtils": [{
			"condition": "OnBeanCondition",
			"message": "@ConditionalOnMissingBean (types: org.springframework.cloud.commons.util.InetUtils; SearchStrategy: all) did not find any beans"
		}],
		"ArchaiusAutoConfiguration": [{
			"condition": "OnClassCondition",
			"message": "@ConditionalOnClass found required classes 'com.netflix.config.ConcurrentCompositeConfiguration', 'org.apache.commons.configuration.ConfigurationBuilder'"
		}],
		"ArchaiusAutoConfiguration.ArchaiusEndpointConfiguration": [{
			"condition": "OnClassCondition",
			"message": "@ConditionalOnClass found required class 'org.springframework.boot.actuate.endpoint.Endpoint'"
		},
		{
			"condition": "OnEnabledEndpointCondition",
			"message": "@ConditionalOnEnabledEndpoint All endpoints are enabled by default"
		}],
		"ArchaiusAutoConfiguration.PropagateEventsConfiguration": [{
			"condition": "OnClassCondition",
			"message": "@ConditionalOnClass found required class 'org.springframework.cloud.context.environment.EnvironmentChangeEvent'"
		},
		{
			"condition": "OnPropertyCondition",
			"message": "@ConditionalOnProperty (archaius.propagate.environmentChangedEvent) matched"
		}],
		"EurekaClientAutoConfiguration": [{
			"condition": "OnClassCondition",
			"message": "@ConditionalOnClass found required class 'com.netflix.discovery.EurekaClientConfig'"
		},
		{
			"condition": "OnPropertyCondition",
			"message": "@ConditionalOnProperty (eureka.client.enabled) matched"
		}],
		"EurekaClientAutoConfiguration#discoveryClientOptionalArgs": [{
			"condition": "OnBeanCondition",
			"message": "@ConditionalOnMissingBean (types: com.netflix.discovery.DiscoveryClient$DiscoveryClientOptionalArgs; SearchStrategy: current) did not find any beans"
		}],
		"EurekaClientAutoConfiguration#eurekaClientConfigBean": [{
			"condition": "OnBeanCondition",
			"message": "@ConditionalOnMissingBean (types: com.netflix.discovery.EurekaClientConfig; SearchStrategy: current) did not find any beans"
		}],
		"EurekaClientAutoConfiguration#eurekaInstanceConfigBean": [{
			"condition": "OnBeanCondition",
			"message": "@ConditionalOnMissingBean (types: com.netflix.appinfo.EurekaInstanceConfig; SearchStrategy: current) did not find any beans"
		}],
		"EurekaClientAutoConfiguration.RefreshableEurekaClientConfiguration": [{
			"condition": "OnClassCondition",
			"message": "@ConditionalOnClass found required class 'org.springframework.cloud.context.scope.refresh.RefreshScope'"
		},
		{
			"condition": "OnBeanCondition",
			"message": "@ConditionalOnBean (types: org.springframework.cloud.autoconfigure.RefreshAutoConfiguration; SearchStrategy: all) found bean 'org.springframework.cloud.autoconfigure.RefreshAutoConfiguration'"
		}],
		"EurekaClientAutoConfiguration.RefreshableEurekaClientConfiguration#eurekaApplicationInfoManager": [{
			"condition": "OnBeanCondition",
			"message": "@ConditionalOnMissingBean (types: com.netflix.appinfo.ApplicationInfoManager; SearchStrategy: current) did not find any beans"
		}],
		"EurekaClientAutoConfiguration.RefreshableEurekaClientConfiguration#eurekaClient": [{
			"condition": "OnBeanCondition",
			"message": "@ConditionalOnMissingBean (types: com.netflix.discovery.EurekaClient; SearchStrategy: current) did not find any beans"
		}],
		"EurekaDiscoveryClientConfiguration": [{
			"condition": "OnClassCondition",
			"message": "@ConditionalOnClass found required class 'com.netflix.discovery.EurekaClientConfig'"
		},
		{
			"condition": "OnPropertyCondition",
			"message": "@ConditionalOnProperty (eureka.client.enabled) matched"
		}],
		"EurekaDiscoveryClientConfiguration.EurekaClientConfigurationRefresher": [{
			"condition": "OnClassCondition",
			"message": "@ConditionalOnClass found required class 'org.springframework.cloud.context.scope.refresh.RefreshScopeRefreshedEvent'"
		}],
		"EurekaDiscoveryClientConfiguration.EurekaHealthIndicatorConfiguration": [{
			"condition": "OnClassCondition",
			"message": "@ConditionalOnClass found required class 'org.springframework.boot.actuate.endpoint.Endpoint'"
		}],
		"EurekaDiscoveryClientConfiguration.EurekaHealthIndicatorConfiguration#eurekaHealthIndicator": [{
			"condition": "OnBeanCondition",
			"message": "@ConditionalOnMissingBean (types: org.springframework.cloud.netflix.eureka.EurekaHealthIndicator; SearchStrategy: all) did not find any beans"
		}],
		"EurekaServerConfiguration#eurekaController": [{
			"condition": "OnPropertyCondition",
			"message": "@ConditionalOnProperty (eureka.dashboard.enabled) matched"
		}],
		"EurekaServerConfiguration.EurekaServerConfigBeanConfiguration#eurekaServerConfig": [{
			"condition": "OnBeanCondition",
			"message": "@ConditionalOnMissingBean (types: com.netflix.eureka.EurekaServerConfig; SearchStrategy: all) did not find any beans"
		}],
		"HystrixAutoConfiguration": [{
			"condition": "OnClassCondition",
			"message": "@ConditionalOnClass found required classes 'com.netflix.hystrix.Hystrix', 'org.springframework.boot.actuate.health.HealthIndicator'"
		}],
		"HystrixAutoConfiguration#hystrixHealthIndicator": [{
			"condition": "OnEnabledHealthIndicatorCondition",
			"message": "@ConditionalOnEnabledHealthIndicator management.health.defaults.enabled is considered true"
		}],
		"MetricsInterceptorConfiguration": [{
			"condition": "OnClassCondition",
			"message": "@ConditionalOnClass found required classes 'com.netflix.servo.monitor.Monitors', 'org.springframework.boot.actuate.metrics.reader.MetricReader'"
		},
		{
			"condition": "OnPropertyCondition",
			"message": "@ConditionalOnProperty (spring.cloud.netflix.metrics.enabled=true) matched"
		}],
		"MetricsInterceptorConfiguration.MetricsWebResourceConfiguration": [{
			"condition": "OnWebApplicationCondition",
			"message": "@ConditionalOnWebApplication (required) found StandardServletEnvironment"
		}],
		"ServoMetricsAutoConfiguration": [{
			"condition": "OnClassCondition",
			"message": "@ConditionalOnClass found required classes 'com.netflix.servo.monitor.Monitors', 'org.springframework.boot.actuate.metrics.reader.MetricReader'; @ConditionalOnMissingClass did not find unwanted class 'com.netflix.spectator.api.Registry'"
		},
		{
			"condition": "OnPropertyCondition",
			"message": "@ConditionalOnProperty (spring.metrics.servo.enabled) matched"
		}],
		"ServoMetricsAutoConfiguration#monitorRegistry": [{
			"condition": "OnBeanCondition",
			"message": "@ConditionalOnMissingBean (types: com.netflix.servo.MonitorRegistry; SearchStrategy: all) did not find any beans"
		}],
		"ServoMetricsAutoConfiguration#servoMetricNaming": [{
			"condition": "OnBeanCondition",
			"message": "@ConditionalOnMissingBean (types: org.springframework.cloud.netflix.metrics.servo.ServoMetricNaming; SearchStrategy: all) did not find any beans"
		}],
		"ServoMetricsAutoConfiguration#servoMetricServices": [{
			"condition": "OnBeanCondition",
			"message": "@ConditionalOnMissingBean (types: org.springframework.boot.actuate.metrics.CounterService,org.springframework.boot.actuate.metrics.GaugeService; SearchStrategy: all) did not find any beans"
		}],
		"ServoMetricsAutoConfiguration#servoMetricsConfig": [{
			"condition": "OnBeanCondition",
			"message": "@ConditionalOnMissingBean (types: org.springframework.cloud.netflix.metrics.servo.ServoMetricsConfigBean; SearchStrategy: all) did not find any beans"
		}],
		"ServoMetricsAutoConfiguration.MetricsTagConfiguration": [{
			"condition": "OnClassCondition",
			"message": "@ConditionalOnClass found required class 'javax.servlet.http.HttpServletRequest'"
		}],
		"RibbonAutoConfiguration": [{
			"condition": "OnClassCondition",
			"message": "@ConditionalOnClass found required classes 'com.netflix.client.IClient', 'org.springframework.web.client.RestTemplate'"
		}],
		"RibbonAutoConfiguration#loadBalancedRetryPolicyFactory": [{
			"condition": "OnClassCondition",
			"message": "@ConditionalOnClass found required class 'org.springframework.retry.support.RetryTemplate'"
		}],
		"RibbonAutoConfiguration#loadBalancerClient": [{
			"condition": "OnBeanCondition",
			"message": "@ConditionalOnMissingBean (types: org.springframework.cloud.client.loadbalancer.LoadBalancerClient; SearchStrategy: all) did not find any beans"
		}],
		"RibbonAutoConfiguration#propertiesFactory": [{
			"condition": "OnBeanCondition",
			"message": "@ConditionalOnMissingBean (types: org.springframework.cloud.netflix.ribbon.PropertiesFactory; SearchStrategy: all) did not find any beans"
		}],
		"RibbonEurekaAutoConfiguration": [{
			"condition": "RibbonEurekaAutoConfiguration.OnRibbonAndEurekaEnabledCondition",
			"message": "AllNestedConditions 2 matched 0 did not; NestedCondition on RibbonEurekaAutoConfiguration.OnRibbonAndEurekaEnabledCondition.EurekaBeans @ConditionalOnBean (types: com.netflix.discovery.EurekaClient; SearchStrategy: all) found bean 'scopedTarget.eurekaClient'; NestedCondition on RibbonEurekaAutoConfiguration.OnRibbonAndEurekaEnabledCondition.Defaults found matching nested conditions @ConditionalOnClass found required class 'com.netflix.niws.loadbalancer.DiscoveryEnabledNIWSServerList', @ConditionalOnBean (types: org.springframework.cloud.netflix.ribbon.SpringClientFactory; SearchStrategy: all) found bean 'springClientFactory', @ConditionalOnProperty (ribbon.eureka.enabled) matched"
		}],
		"RxJavaAutoConfiguration": [{
			"condition": "OnClassCondition",
			"message": "@ConditionalOnClass found required class 'rx.Observable'"
		},
		{
			"condition": "OnWebApplicationCondition",
			"message": "@ConditionalOnWebApplication (required) found StandardServletEnvironment"
		}],
		"RxJavaAutoConfiguration.RxJavaReturnValueHandlerConfig": [{
			"condition": "OnClassCondition",
			"message": "@ConditionalOnClass found required class 'org.springframework.web.method.support.AsyncHandlerMethodReturnValueHandler'"
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
			"message": "@ConditionalOnClass did not find required class 'com.github.benmanes.caffeine.cache.Caffeine'"
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
			"message": "@ConditionalOnClass did not find required classes 'net.sf.ehcache.Ehcache', 'net.sf.ehcache.statistics.StatisticsGateway'"
		},
		{
			"condition": "ConditionEvaluationReport.AncestorsMatchedCondition",
			"message": "Ancestor org.springframework.boot.actuate.autoconfigure.CacheStatisticsAutoConfiguration did not match"
		}],
		"CacheStatisticsAutoConfiguration.GuavaCacheStatisticsConfiguration": [{
			"condition": "OnClassCondition",
			"message": "@ConditionalOnClass found required classes 'com.google.common.cache.Cache', 'org.springframework.cache.guava.GuavaCache'"
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
			"message": "@ConditionalOnClass did not find required class 'javax.cache.Caching'"
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
			"message": "@ConditionalOnMissingBean (types: org.springframework.boot.actuate.health.HealthIndicator; SearchStrategy: all) found beans 'discoveryCompositeHealthIndicator', 'diskSpaceHealthIndicator'"
		}],
		"HealthIndicatorAutoConfiguration.CassandraHealthIndicatorConfiguration": [{
			"condition": "OnClassCondition",
			"message": "@ConditionalOnClass did not find required classes 'org.springframework.data.cassandra.core.CassandraOperations', 'com.datastax.driver.core.Cluster'"
		}],
		"HealthIndicatorAutoConfiguration.CouchbaseHealthIndicatorConfiguration": [{
			"condition": "OnClassCondition",
			"message": "@ConditionalOnClass did not find required classes 'org.springframework.data.couchbase.core.CouchbaseOperations', 'com.couchbase.client.java.Bucket'"
		}],
		"HealthIndicatorAutoConfiguration.DataSourcesHealthIndicatorConfiguration": [{
			"condition": "OnClassCondition",
			"message": "@ConditionalOnClass did not find required class 'org.springframework.jdbc.core.JdbcTemplate'"
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
		"MetricRepositoryAutoConfiguration.FastMetricServicesConfiguration": [{
			"condition": "OnJavaCondition",
			"message": "@ConditionalOnJava (1.8 or newer) found 1.8"
		},
		{
			"condition": "OnBeanCondition",
			"message": "@ConditionalOnMissingBean (types: org.springframework.boot.actuate.metrics.GaugeService; SearchStrategy: all) found bean 'servoMetricServices'"
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
		"PublicMetricsAutoConfiguration.DataSourceMetricsConfiguration": [{
			"condition": "OnClassCondition",
			"message": "@ConditionalOnClass found required class 'javax.sql.DataSource'"
		},
		{
			"condition": "OnBeanCondition",
			"message": "@ConditionalOnBean (types: javax.sql.DataSource; SearchStrategy: all) did not find any beans"
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
		"AopAutoConfiguration.JdkDynamicAutoProxyConfiguration": [{
			"condition": "OnPropertyCondition",
			"message": "@ConditionalOnProperty (spring.aop.proxy-target-class=false) found different value in property 'proxy-target-class'"
		}],
		"BatchAutoConfiguration": [{
			"condition": "OnClassCondition",
			"message": "@ConditionalOnClass did not find required classes 'org.springframework.batch.core.launch.JobLauncher', 'org.springframework.jdbc.core.JdbcOperations'"
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
			"message": "@ConditionalOnClass did not find required class 'org.springframework.orm.jpa.LocalContainerEntityManagerFactoryBean'"
		},
		{
			"condition": "ConditionEvaluationReport.AncestorsMatchedCondition",
			"message": "Ancestor org.springframework.boot.autoconfigure.cache.CacheAutoConfiguration did not match"
		}],
		"CaffeineCacheConfiguration": [{
			"condition": "OnClassCondition",
			"message": "@ConditionalOnClass did not find required class 'com.github.benmanes.caffeine.cache.Caffeine'"
		}],
		"CouchbaseCacheConfiguration": [{
			"condition": "OnClassCondition",
			"message": "@ConditionalOnClass did not find required classes 'com.couchbase.client.java.Bucket', 'com.couchbase.client.spring.cache.CouchbaseCacheManager'"
		}],
		"EhCacheCacheConfiguration": [{
			"condition": "OnClassCondition",
			"message": "@ConditionalOnClass did not find required class 'net.sf.ehcache.Cache'"
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
			"message": "@ConditionalOnClass did not find required class 'javax.cache.Caching'"
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
		"PersistenceExceptionTranslationAutoConfiguration": [{
			"condition": "OnClassCondition",
			"message": "@ConditionalOnClass did not find required class 'org.springframework.dao.annotation.PersistenceExceptionTranslationPostProcessor'"
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
		"JpaRepositoriesAutoConfiguration": [{
			"condition": "OnClassCondition",
			"message": "@ConditionalOnClass did not find required class 'org.springframework.data.jpa.repository.JpaRepository'"
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
		"SpringDataWebAutoConfiguration": [{
			"condition": "OnClassCondition",
			"message": "@ConditionalOnClass did not find required class 'org.springframework.data.web.PageableHandlerMethodArgumentResolver'"
		}],
		"JestAutoConfiguration": [{
			"condition": "OnClassCondition",
			"message": "@ConditionalOnClass did not find required class 'io.searchbox.client.JestClient'"
		}],
		"FlywayAutoConfiguration": [{
			"condition": "OnClassCondition",
			"message": "@ConditionalOnClass did not find required class 'org.flywaydb.core.Flyway'"
		}],
		"FreeMarkerAutoConfiguration.FreeMarkerNonWebConfiguration": [{
			"condition": "OnWebApplicationCondition",
			"message": "@ConditionalOnWebApplication found StandardServletEnvironment"
		}],
		"FreeMarkerAutoConfiguration.FreeMarkerWebConfiguration#resourceUrlEncodingFilter": [{
			"condition": "OnBeanCondition",
			"message": "@ConditionalOnMissingBean (types: org.springframework.web.servlet.resource.ResourceUrlEncodingFilter; SearchStrategy: all) did not find any beans"
		},
		{
			"condition": "OnEnabledResourceChainCondition",
			"message": "@ConditionalOnEnabledResourceChain did not find class org.webjars.WebJarAssetLocator"
		}],
		"GroovyTemplateAutoConfiguration": [{
			"condition": "OnClassCondition",
			"message": "@ConditionalOnClass did not find required class 'groovy.text.markup.MarkupTemplateEngine'"
		}],
		"H2ConsoleAutoConfiguration": [{
			"condition": "OnClassCondition",
			"message": "@ConditionalOnClass did not find required class 'org.h2.server.web.WebServlet'"
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
			"message": "@ConditionalOnClass did not find required classes 'com.hazelcast.core.HazelcastInstance', 'org.springframework.orm.jpa.LocalContainerEntityManagerFactoryBean'"
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
			"message": "@ConditionalOnClass did not find required classes 'com.fasterxml.jackson.datatype.joda.ser.DateTimeSerializer', 'com.fasterxml.jackson.datatype.joda.cfg.JacksonJodaDateFormat'"
		}],
		"JacksonAutoConfiguration.ParameterNamesModuleConfiguration": [{
			"condition": "OnClassCondition",
			"message": "@ConditionalOnClass did not find required class 'com.fasterxml.jackson.module.paramnames.ParameterNamesModule'"
		}],
		"DataSourceAutoConfiguration": [{
			"condition": "OnClassCondition",
			"message": "@ConditionalOnClass did not find required class 'org.springframework.jdbc.datasource.embedded.EmbeddedDatabaseType'"
		}],
		"DataSourceTransactionManagerAutoConfiguration": [{
			"condition": "OnClassCondition",
			"message": "@ConditionalOnClass did not find required classes 'org.springframework.jdbc.core.JdbcTemplate', 'org.springframework.transaction.PlatformTransactionManager'"
		}],
		"JdbcTemplateAutoConfiguration": [{
			"condition": "OnClassCondition",
			"message": "@ConditionalOnClass did not find required class 'org.springframework.jdbc.core.JdbcTemplate'"
		}],
		"JndiDataSourceAutoConfiguration": [{
			"condition": "OnClassCondition",
			"message": "@ConditionalOnClass did not find required class 'org.springframework.jdbc.datasource.embedded.EmbeddedDatabaseType'"
		}],
		"XADataSourceAutoConfiguration": [{
			"condition": "OnClassCondition",
			"message": "@ConditionalOnClass did not find required classes 'javax.transaction.TransactionManager', 'org.springframework.jdbc.datasource.embedded.EmbeddedDatabaseType'"
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
		"HibernateJpaAutoConfiguration": [{
			"condition": "OnClassCondition",
			"message": "@ConditionalOnClass did not find required classes 'org.springframework.orm.jpa.LocalContainerEntityManagerFactoryBean', 'org.springframework.transaction.annotation.EnableTransactionManagement', 'javax.persistence.EntityManager'"
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
		"TransactionAutoConfiguration": [{
			"condition": "OnClassCondition",
			"message": "@ConditionalOnClass did not find required classes 'org.springframework.transaction.support.TransactionTemplate', 'org.springframework.transaction.PlatformTransactionManager'"
		}],
		"JtaAutoConfiguration": [{
			"condition": "OnClassCondition",
			"message": "@ConditionalOnClass did not find required class 'javax.transaction.Transaction'"
		}],
		"VelocityAutoConfiguration": [{
			"condition": "OnClassCondition",
			"message": "@ConditionalOnClass did not find required class 'org.apache.velocity.app.VelocityEngine'"
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
		"GsonHttpMessageConvertersConfiguration.GsonHttpMessageConverterConfiguration": [{
			"condition": "GsonHttpMessageConvertersConfiguration.PreferGsonOrMissingJacksonCondition",
			"message": "AnyNestedCondition 0 matched 2 did not; NestedCondition on GsonHttpMessageConvertersConfiguration.PreferGsonOrMissingJacksonCondition.JacksonMissing @ConditionalOnMissingBean (types: org.springframework.http.converter.json.MappingJackson2HttpMessageConverter; SearchStrategy: all) found bean 'mappingJackson2HttpMessageConverter'; NestedCondition on GsonHttpMessageConvertersConfiguration.PreferGsonOrMissingJacksonCondition.GsonPreferred @ConditionalOnProperty (spring.http.converters.preferred-json-mapper=gson) did not find property 'spring.http.converters.preferred-json-mapper'"
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
		}],
		"RefreshEndpointAutoConfiguration.InfoEndpointAutoConfiguration": [{
			"condition": "OnClassCondition",
			"message": "@ConditionalOnMissingClass found unwanted class 'org.springframework.boot.actuate.info.InfoContributor'"
		}],
		"RefreshEndpointAutoConfiguration.RestartEndpointWithIntegration": [{
			"condition": "OnClassCondition",
			"message": "@ConditionalOnClass did not find required class 'org.springframework.integration.monitor.IntegrationMBeanExporter'"
		}],
		"NoopDiscoveryClientAutoConfiguration": [{
			"condition": "OnBeanCondition",
			"message": "@ConditionalOnMissingBean (types: org.springframework.cloud.client.discovery.DiscoveryClient; SearchStrategy: all) found bean 'discoveryClient'"
		}],
		"CloudHypermediaAutoConfiguration": [{
			"condition": "OnBeanCondition",
			"message": "@ConditionalOnBean (types: org.springframework.cloud.client.hypermedia.RemoteResource; SearchStrategy: all) did not find any beans"
		}],
		"LoadBalancerAutoConfiguration.LoadBalancerInterceptorConfig": [{
			"condition": "OnClassCondition",
			"message": "@ConditionalOnMissingClass found unwanted class 'org.springframework.retry.support.RetryTemplate'"
		}],
		"LoadBalancerAutoConfiguration.RetryAutoConfiguration#loadBalancedRetryPolicyFactory": [{
			"condition": "OnBeanCondition",
			"message": "@ConditionalOnMissingBean (types: org.springframework.cloud.client.loadbalancer.LoadBalancedRetryPolicyFactory; SearchStrategy: all) found bean 'loadBalancedRetryPolicyFactory'"
		}],
		"EurekaClientAutoConfiguration.EurekaClientConfiguration": [{
			"condition": "EurekaClientAutoConfiguration.OnMissingRefreshScopeCondition",
			"message": "AnyNestedCondition 0 matched 2 did not; NestedCondition on EurekaClientAutoConfiguration.OnMissingRefreshScopeCondition.MissingScope @ConditionalOnMissingBean (types: org.springframework.cloud.autoconfigure.RefreshAutoConfiguration; SearchStrategy: all) found bean 'org.springframework.cloud.autoconfigure.RefreshAutoConfiguration'; NestedCondition on EurekaClientAutoConfiguration.OnMissingRefreshScopeCondition.MissingClass @ConditionalOnMissingClass found unwanted class 'org.springframework.cloud.context.scope.refresh.RefreshScope'"
		}],
		"EurekaDiscoveryClientConfiguration.EurekaHealthCheckHandlerConfiguration": [{
			"condition": "OnPropertyCondition",
			"message": "@ConditionalOnProperty (eureka.client.healthcheck.enabled) did not find property 'eureka.client.healthcheck.enabled'"
		}],
		"EurekaClientConfigServerAutoConfiguration": [{
			"condition": "OnClassCondition",
			"message": "@ConditionalOnClass did not find required class 'org.springframework.cloud.config.server.config.ConfigServerProperties'"
		}],
		"EurekaDiscoveryClientConfigServiceAutoConfiguration": [{
			"condition": "OnPropertyCondition",
			"message": "@ConditionalOnProperty (spring.cloud.config.discovery.enabled) did not find property 'spring.cloud.config.discovery.enabled'"
		}],
		"FeignAutoConfiguration": [{
			"condition": "OnClassCondition",
			"message": "@ConditionalOnClass did not find required class 'feign.Feign'"
		}],
		"FeignAcceptGzipEncodingAutoConfiguration": [{
			"condition": "OnClassCondition",
			"message": "@ConditionalOnClass did not find required class 'feign.Feign'"
		}],
		"FeignContentGzipEncodingAutoConfiguration": [{
			"condition": "OnClassCondition",
			"message": "@ConditionalOnClass did not find required class 'feign.Feign'"
		}],
		"FeignRibbonClientAutoConfiguration": [{
			"condition": "OnClassCondition",
			"message": "@ConditionalOnClass did not find required class 'feign.Feign'"
		}],
		"HystrixSecurityAutoConfiguration": [{
			"condition": "OnClassCondition",
			"message": "@ConditionalOnClass did not find required class 'org.springframework.security.core.context.SecurityContext'"
		}],
		"MetricsInterceptorConfiguration.MetricsRestTemplateAspectConfiguration": [{
			"condition": "OnClassCondition",
			"message": "@ConditionalOnClass found required class 'org.aspectj.lang.JoinPoint'"
		},
		{
			"condition": "OnPropertyCondition",
			"message": "@ConditionalOnProperty (spring.aop.enabled=true) matched"
		},
		{
			"condition": "OnBeanCondition",
			"message": "@ConditionalOnBean (types: org.springframework.web.client.RestTemplate; SearchStrategy: all) did not find any beans"
		}],
		"MetricsInterceptorConfiguration.MetricsRestTemplateConfiguration": [{
			"condition": "OnClassCondition",
			"message": "@ConditionalOnClass found required class 'javax.servlet.http.HttpServletRequest'"
		},
		{
			"condition": "OnBeanCondition",
			"message": "@ConditionalOnBean (types: org.springframework.web.client.RestTemplate; SearchStrategy: all) did not find any beans"
		}],
		"RibbonAutoConfiguration.RibbonClientConfig": [{
			"condition": "OnClassCondition",
			"message": "@ConditionalOnClass found required class 'com.netflix.client.http.HttpRequest'"
		},
		{
			"condition": "RibbonAutoConfiguration.OnRibbonRestClientCondition",
			"message": "AnyNestedCondition 0 matched 2 did not; NestedCondition on RibbonAutoConfiguration.OnRibbonRestClientCondition.RibbonProperty @ConditionalOnProperty (ribbon.restclient.enabled) did not find property 'ribbon.restclient.enabled'; NestedCondition on RibbonAutoConfiguration.OnRibbonRestClientCondition.ZuulProperty @ConditionalOnProperty (ribbon.http.client.enabled) did not find property 'ribbon.http.client.enabled'"
		}]
	},
	"parent": {
		"positiveMatches": {
			"PropertyPlaceholderAutoConfiguration#propertySourcesPlaceholderConfigurer": [{
				"condition": "OnBeanCondition",
				"message": "@ConditionalOnMissingBean (types: org.springframework.context.support.PropertySourcesPlaceholderConfigurer; SearchStrategy: current) did not find any beans"
			}],
			"ConfigurationPropertiesRebinderAutoConfiguration": [{
				"condition": "OnBeanCondition",
				"message": "@ConditionalOnBean (types: org.springframework.boot.context.properties.ConfigurationPropertiesBindingPostProcessor; SearchStrategy: all) found bean 'org.springframework.boot.context.properties.ConfigurationPropertiesBindingPostProcessor'"
			}],
			"ConfigurationPropertiesRebinderAutoConfiguration#configurationPropertiesBeans": [{
				"condition": "OnBeanCondition",
				"message": "@ConditionalOnMissingBean (types: org.springframework.cloud.context.properties.ConfigurationPropertiesBeans; SearchStrategy: current) did not find any beans"
			}],
			"ConfigurationPropertiesRebinderAutoConfiguration#configurationPropertiesRebinder": [{
				"condition": "OnBeanCondition",
				"message": "@ConditionalOnMissingBean (types: org.springframework.cloud.context.properties.ConfigurationPropertiesRebinder; SearchStrategy: current) did not find any beans"
			}],
			"EncryptionBootstrapConfiguration": [{
				"condition": "OnClassCondition",
				"message": "@ConditionalOnClass found required class 'org.springframework.security.crypto.encrypt.TextEncryptor'"
			}]
		},
		"negativeMatches": {
			"EncryptionBootstrapConfiguration.RsaEncryptionConfiguration": [{
				"condition": "OnClassCondition",
				"message": "@ConditionalOnClass found required class 'org.springframework.security.rsa.crypto.RsaSecretEncryptor'"
			},
			{
				"condition": "EncryptionBootstrapConfiguration.KeyCondition",
				"message": "Keystore nor key found in Environment"
			}],
			"EncryptionBootstrapConfiguration.VanillaEncryptionConfiguration": [{
				"condition": "OnClassCondition",
				"message": "@ConditionalOnMissingClass found unwanted class 'org.springframework.security.rsa.crypto.RsaSecretEncryptor'"
			}]
		}
	}
}