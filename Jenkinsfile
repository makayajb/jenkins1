 pipeline {
    agent any
    stages {
        stage('Build et Test') {
            steps {
                echo 'Build et Test'
            }
        }
        stage('Déploiement en Production') {
            input {
                message "Voulez-vous déployer en production ?"
                ok "Oui, déployons."
                submitter "admin,devops"
                parameters {
                    string(name: 'VERSION', defaultValue: 'latest', description: 'Quelle version souhaitez-vous déployer ?')
                }
            }
            steps {
                echo "Déploiement de la version ${VERSION} en production."
                // Votre code pour le déploiement
            }
        }
    }
}
 