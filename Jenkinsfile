pipeline{
    agent any

    stages {
        stage('Teste arquivo'){
            steps {
                script {
                    def arquivoCsvPath = input message: 'Carregar arquivo CSV', parameters: [file(name: 'teste_file.csv', description: 'Apenas arquivos CSV')]
                    def arquivo = readFile "${arquivoCsvPath}"
                    
                    echo ("Csv:" + arquivo)
                    
                    arquivo.split('\n').each { line, count ->
                    	def fields = line.split(";")    
                    	
                    	echo ("fieeeelds: " + fields[0])                		
                    }
                }
                
                echo env.STAGE_NAME
                echo '=========== Carregar CSV ============'
            }
       }
   }
}
