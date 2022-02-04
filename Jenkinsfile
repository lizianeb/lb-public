pipeline{
    agent any

    stages {
        stage('Teste arquivo'){
            steps {
                script {
                    def arquivoCsvPath = input message: 'Carregar arquivo csv', parameters: [file(name: 'teste_file.csv', description: 'Apenas arquivos CSV')]
                    def content = readFile "${arquivoCsvPath}"
                    
                    echo ("Arquivo csv caminho: ${arquivoCsvPath}")
                    echo ("Csv: ${content}")
                }
                echo env.STAGE_NAME
                echo '=========== Carregar CSV ============'
            }
        }
    }
}
