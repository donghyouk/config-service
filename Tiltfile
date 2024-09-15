custom_build(
    ref = 'config-server',
    command = './mvnw spring-boot:build-image -DimageName=$EXPECTED_REF',
    deps = ['pom.xml', 'src']
)

k8s_yaml(['k8s/deployment.yml', 'k8s/service.yml'])

k8s_resource('config-server', port_forwards=['8888'])
