pipeline{
    agent any

    stages {
        stage('Teste arquivo'){
            steps {
                script {
                    def arquivoCsvPath = input message: 'Carregar arquivo CSV', parameters: [file(name: 'teste_file.csv', description: 'Apenas arquivos CSV')]
                    def conteudoArquivoCsv = readFile "${arquivoCsvPath}"
                    
                    echo ("Csv: ${conteudoArquivoCsv}")
                    
                    conteudoArquivoCsv.split('\n').each { line, count ->
                    def fields = line.split(';')
                    
                    for(String item: fields) {
                    	println item
                    	println 'Linha:' + count
                    }
                    nodes["line${count}"] = {
                    	node {
                    		echo fields[0] + ':' + fields[1] + ':' + fields[2];
                    	}
                    }
                }
                echo env.STAGE_NAME
                echo '=========== Carregar CSV ============'
            }
        }
    }
}
