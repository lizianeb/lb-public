pipeline{
    agent any

    stages {
        stage('Teste arquivo'){
            steps {
                script {
                    def arquivoCsvPath = input message: 'Carregar arquivo CSV', parameters: [file(name: 'teste_file.csv', description: 'Apenas arquivos CSV')]
                    def conteudoArquivoCsv = readFile "${arquivoCsvPath}"
                    
                    def arquivo = "${conteudoArquivoCsv}"
                    echo ("Csv:" + arquivo)
                    
                    readFile(arquivo).eachLine { line ->
                    	def fields = line.split(';').each { value ->
                    		echo ("Tessste: ${value}")
                    	}
                    }
                }
                
                echo env.STAGE_NAME
                echo '=========== Carregar CSV ============'
            }
       }
   }
}
