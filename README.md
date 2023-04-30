base URL : https://json-serve-travel-planner.onrender.com


#LOGIN USER/POST
post
baseUrl/login {corpo da requisição}


#REGISTER USER/POST
post
baseUrl/register {corpo da requisição}


#ACESSAR VIAGEM/GET
get
baseUrl/travel token
"obs - dessa forma só mostra  a viagem em questão"


#ACESSAR VIAGEM USUÁRIO LOGADO/GET
GET
baseUrl/users/{idUser}?_embed=travel + token
"obs - dessa forma mostra uma key no user logado (travel), e nela tem os dados da viagem


#CRIAR VIAGEM/POST
post
baseUrl/travel {corpo da requisição, dentro do corpo o id do user} + token


#DELETAR VIAGEM/DELETE
delete
baseUrl/tavel/{idViagem} + token


#EDITAR VIAGEM/PATCH
patch
baseUrl/tavel/{idViagem}  {corpo da requisição} + token
{obs o corpo da requisição pode mandar sem ser completo, exemplo, quero editar só o preço da passagem}


#ADD VALOR E MÊS/POST
baseUrl/savings  {corpo da requisição} + token

OBS PRECISA QUE O ID DO USUARIO E O ID DO TRAVEL SEJA PASSADO NO CORPO DA REQUISIÇÃO EX:
{
	"month": "julho",
	"value": 900,
	"userId": 2,
	"travelId": 2,
	"id": 3
}
