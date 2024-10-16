custom_build(
    ref = 'config-service',
    command = './mvnw spring-boot:build-image -DimageName=$EXPECTED_REF',
    deps = ['pom.xml', 'src']
)

k8s_yaml(['k8s/deployment.yml', 'k8s/service.yml'])

k8s_resource('config-service', port_forwards=['8888'])
