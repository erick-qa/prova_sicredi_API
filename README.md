# Teste de API

* O arquivo "Prova_Sicredi_API.postman_collection.json" é onde estão contidos todos os testes. Para rodar basta ter o programa Postman instalado, importar esse arquivo e executar a collection, o arquivo "Prova_Sicredi_API.postman_test_run.json" é onde estão contidos todos os resultados descritos abaixo, mas podem ser obtidos apenas executando a collection.

* Os 10 CPF'S da documentação informam que tem restrição, mas o resultado da API foi "204", resultando que não possuem restrição. Sendo assim, todos os testes falharam.

* Para os testes de cadastramento de simulação, foram realizados da seguinte maneira:

```bash
Duas simulações efetuadas de forma correta que retornaram status 201.
```
```bash
Uma simulação com 50 parcelas (fora da regra de negócio) que não retornou erro 400, e sim 201. Sendo assim, o teste falhou.
```
```bash
E uma simulação com o mesmo CPF da primeira simulação, que não retornou erro 409, e sim 400. Sendo assim, o teste falhou.
```

* O teste de alteração não teve resposta 200, e sim 404, API retornou que o CPF da primeira simulação cadastrada não foi encontrado. Sendo assim, o teste falhou.

* A consulta de todas as simulações retornou status 200 e passou.

* A consulta de uma simulação por CPF não teve resposta 200 e sim 404, sendo que foi a primeira simulação cadastrada.

* E o deletar usuário não teve resposta 204 e sim 400, tendo falhado, pois era uma simulação que já estava cadastrada.
 
