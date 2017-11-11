{
	"/webjars/**": {
		"bean": "resourceHandlerMapping"
	},
	"/**": {
		"bean": "resourceHandlerMapping"
	},
	"/**/favicon.ico": {
		"bean": "faviconHandlerMapping"
	},
	"{[/],methods=[GET]}": {
		"bean": "requestMappingHandlerMapping",
		"method": "public java.lang.String org.springframework.cloud.netflix.eureka.server.EurekaController.status(javax.servlet.http.HttpServletRequest,java.util.Map<java.lang.String, java.lang.Object>)"
	},
	"{[/lastn],methods=[GET]}": {
		"bean": "requestMappingHandlerMapping",
		"method": "public java.lang.String org.springframework.cloud.netflix.eureka.server.EurekaController.lastn(javax.servlet.http.HttpServletRequest,java.util.Map<java.lang.String, java.lang.Object>)"
	},
	"{[/error]}": {
		"bean": "requestMappingHandlerMapping",
		"method": "public org.springframework.http.ResponseEntity<java.util.Map<java.lang.String, java.lang.Object>> org.springframework.boot.autoconfigure.web.BasicErrorController.error(javax.servlet.http.HttpServletRequest)"
	},
	"{[/error],produces=[text/html]}": {
		"bean": "requestMappingHandlerMapping",
		"method": "public org.springframework.web.servlet.ModelAndView org.springframework.boot.autoconfigure.web.BasicErrorController.errorHtml(javax.servlet.http.HttpServletRequest,javax.servlet.http.HttpServletResponse)"
	},
	"{[/trace || /trace.json],methods=[GET],produces=[application/json]}": {
		"bean": "endpointHandlerMapping",
		"method": "public java.lang.Object org.springframework.boot.actuate.endpoint.mvc.EndpointMvcAdapter.invoke()"
	},
	"{[/dump || /dump.json],methods=[GET],produces=[application/json]}": {
		"bean": "endpointHandlerMapping",
		"method": "public java.lang.Object org.springframework.boot.actuate.endpoint.mvc.EndpointMvcAdapter.invoke()"
	},
	"{[/pause || /pause.json],methods=[POST]}": {
		"bean": "endpointHandlerMapping",
		"method": "public java.lang.Object org.springframework.cloud.endpoint.GenericPostableMvcEndpoint.invoke()"
	},
	"{[/archaius || /archaius.json],methods=[GET],produces=[application/json]}": {
		"bean": "endpointHandlerMapping",
		"method": "public java.lang.Object org.springframework.boot.actuate.endpoint.mvc.EndpointMvcAdapter.invoke()"
	},
	"{[/info || /info.json],methods=[GET],produces=[application/json]}": {
		"bean": "endpointHandlerMapping",
		"method": "public java.lang.Object org.springframework.boot.actuate.endpoint.mvc.EndpointMvcAdapter.invoke()"
	},
	"{[/env/{name:.*}],methods=[GET],produces=[application/json]}": {
		"bean": "endpointHandlerMapping",
		"method": "public java.lang.Object org.springframework.boot.actuate.endpoint.mvc.EnvironmentMvcEndpoint.value(java.lang.String)"
	},
	"{[/env || /env.json],methods=[GET],produces=[application/json]}": {
		"bean": "endpointHandlerMapping",
		"method": "public java.lang.Object org.springframework.boot.actuate.endpoint.mvc.EndpointMvcAdapter.invoke()"
	},
	"{[/beans || /beans.json],methods=[GET],produces=[application/json]}": {
		"bean": "endpointHandlerMapping",
		"method": "public java.lang.Object org.springframework.boot.actuate.endpoint.mvc.EndpointMvcAdapter.invoke()"
	},
	"{[/health || /health.json],produces=[application/json]}": {
		"bean": "endpointHandlerMapping",
		"method": "public java.lang.Object org.springframework.boot.actuate.endpoint.mvc.HealthMvcEndpoint.invoke(java.security.Principal)"
	},
	"{[/configprops || /configprops.json],methods=[GET],produces=[application/json]}": {
		"bean": "endpointHandlerMapping",
		"method": "public java.lang.Object org.springframework.boot.actuate.endpoint.mvc.EndpointMvcAdapter.invoke()"
	},
	"{[/resume || /resume.json],methods=[POST]}": {
		"bean": "endpointHandlerMapping",
		"method": "public java.lang.Object org.springframework.cloud.endpoint.GenericPostableMvcEndpoint.invoke()"
	},
	"{[/heapdump || /heapdump.json],methods=[GET],produces=[application/octet-stream]}": {
		"bean": "endpointHandlerMapping",
		"method": "public void org.springframework.boot.actuate.endpoint.mvc.HeapdumpMvcEndpoint.invoke(boolean,javax.servlet.http.HttpServletRequest,javax.servlet.http.HttpServletResponse) throws java.io.IOException,javax.servlet.ServletException"
	},
	"{[/autoconfig || /autoconfig.json],methods=[GET],produces=[application/json]}": {
		"bean": "endpointHandlerMapping",
		"method": "public java.lang.Object org.springframework.boot.actuate.endpoint.mvc.EndpointMvcAdapter.invoke()"
	},
	"{[/env],methods=[POST]}": {
		"bean": "endpointHandlerMapping",
		"method": "public java.lang.Object org.springframework.cloud.context.environment.EnvironmentManagerMvcEndpoint.value(java.util.Map<java.lang.String, java.lang.String>)"
	},
	"{[/env/reset],methods=[POST]}": {
		"bean": "endpointHandlerMapping",
		"method": "public java.util.Map<java.lang.String, java.lang.Object> org.springframework.cloud.context.environment.EnvironmentManagerMvcEndpoint.reset()"
	},
	"{[/features || /features.json],methods=[GET],produces=[application/json]}": {
		"bean": "endpointHandlerMapping",
		"method": "public java.lang.Object org.springframework.boot.actuate.endpoint.mvc.EndpointMvcAdapter.invoke()"
	},
	"{[/metrics/{name:.*}],methods=[GET],produces=[application/json]}": {
		"bean": "endpointHandlerMapping",
		"method": "public java.lang.Object org.springframework.boot.actuate.endpoint.mvc.MetricsMvcEndpoint.value(java.lang.String)"
	},
	"{[/metrics || /metrics.json],methods=[GET],produces=[application/json]}": {
		"bean": "endpointHandlerMapping",
		"method": "public java.lang.Object org.springframework.boot.actuate.endpoint.mvc.EndpointMvcAdapter.invoke()"
	},
	"{[/refresh || /refresh.json],methods=[POST]}": {
		"bean": "endpointHandlerMapping",
		"method": "public java.lang.Object org.springframework.cloud.endpoint.GenericPostableMvcEndpoint.invoke()"
	},
	"{[/restart || /restart.json],methods=[POST]}": {
		"bean": "endpointHandlerMapping",
		"method": "public java.lang.Object org.springframework.cloud.context.restart.RestartMvcEndpoint.invoke()"
	},
	"{[/mappings || /mappings.json],methods=[GET],produces=[application/json]}": {
		"bean": "endpointHandlerMapping",
		"method": "public java.lang.Object org.springframework.boot.actuate.endpoint.mvc.EndpointMvcAdapter.invoke()"
	}
}