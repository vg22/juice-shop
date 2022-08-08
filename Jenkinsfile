pipeline {
    agent any

    stages {
        stage("Synk Scan") {
            steps {
                script {
                  snykScan {
                      snykInstallation: 'SnykV2PluginTest',
                      snykTokenId: "#{SNYK_TOKEN}",
                      severity_check='high'
                      fail_build=false
                      extra_params='--all-projects --code -d'
                    }
                }
            }
        }
    }
}