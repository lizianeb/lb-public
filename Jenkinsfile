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
                    
                    arquivo.split('\n').each { line, count ->
                    	def fields = line.split(";")    
                    	
                    	echo ("linha: " + line)
                    	echo ("fieeeelds: " + fields)                		
                    	
                    	for(String item: fields){
                    		echo ("tessste: " + item)
                    	}
                    }
                }
                
                echo env.STAGE_NAME
                echo '=========== Carregar CSV ============'
            }
       }
   }
}
