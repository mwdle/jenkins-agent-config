boolean disableIndexTriggers = env.BRANCH_NAME != 'main'

quadletPipeline(
    disableIndexTriggers: disableIndexTriggers,
    podmanSecretMappings: [
        [
            type: 'string',
            credentialsId: 'jenkins-agent-secret',
            podmanSecretStringName: 'jenkins_agent_secret'
        ]
    ]
)
