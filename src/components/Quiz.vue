<template>
	<section>
	<div class="menu">
		<h1 class="menu-titulo">Você sabe?</h1>
				<p v-on:click="addmeioambiente">Meio Ambiente</p>
				<p v-on:click="addsaude">Saúde</p>
				<p v-on:click="addconsumoconsciente">Consumo consciente</p>
	</div>
	<div >
		<ul v-for="value in consumoConsciente" v-if="quest='Consumo'">
			<li>
				<div>
					<h2>{{ value.pergunta}}</h2>
				</div>
				<div>
					
						<div class="casa">
							<p >{{value.alternativa1.texto.fundo}}</p>
						</div>
				 	<div class="casa" >
				 		<p >{{value.alternativa2.texto}}</p>
				 	</div>
					<div class="casa">
						<p>{{value.alternativa3.texto}}</p>
					</div>
				</div>
			</li>
		</ul>
		<ul v-for="value in saude" v-else-if="quest='saude'">
			<li>
				<div>
					<h2>{{ value.pergunta}}</h2>
				</div>
				<div>
					<div class="casa">
						<p>{{value.alternativa1.texto}}</p>
					</div>
				 	<div class="casa" >
				 		<p>{{value.alternativa2.texto}}</p>
				 	</div>
					<div class="casa">
						<p>{{value.alternativa3.texto}}</p>
					</div>
				</div>
			</li>
		</ul>
		<ul v-for="value in meioambientee" v-else>
			<li>
				<div>
					<h2>{{ value.pergunta}}</h2>
				</div>
				<div>
					<div class="casa">
						<p>{{value.alternativa1.texto}}</p>
					</div>
				 	<div class="casa" >
				 		<p>{{value.alternativa2.texto}}</p>
				 	</div>
					<div class="casa">
						<p>{{value.alternativa3.texto}}</p>
					</div>
				</div>
			</li>
		</ul>
	</div>
	
	</section>	
</template>	
<script >
	export default{
		name: 'Quiz',
		data (){
			return{
				preenchimento:'',
				quest:'',
				consumoConsciente: [
					{
						pergunta:"O que pode ser atraído pelo descarte incorreto de alimentos nas lixeiras e encosta?",
						alternativa1:{
							texto:"rato",
							fundo:"../assets/rato.jpg"
						},
						alternativa2:{
							texto:"barata",
							fundo:"../assets/barata.jpg"
						},
							
						alternativa3:{
							texto:"todas as alternativas",
							fundo:""
						}	
					},

					{
						pergunta: " Quando apaga uma lâmpada para economizar energia, você está gerando?",
						alternativa1:{
							texto:"Consumo Consciente",
							fundo:""
						},

						alternativa2:{
							texto:"Cuidado com o consumo exagerado",
							fundo:""
						},	
						alternativa3:{
							texto:"Desperdício de energia elétrica",
							fundo:""
						}
					},
					{
						pergunta: "Qual a quantidade de lixo que um habitante gera por dia no Rio de Janeiro? ",
						alternativa1:{
							texto:"3 Kg",
							fundo:""
						},
						alternativa2:{
							texto:"2,5 Kg",	
							fundo:""
						},
						alternativa3:{
							texto:"1,86",
							fundo:""
						}
					}
 				],
 				saude:[
 					{
 						pergunta:"O que é preciso fazer para evitar um foco de mosquito ?",
 						alternativa1:{
 							texto:"Não deixe água parada",
 							fundo:""
 						},
 						alternativa2:{
 							texto:"Deixar que o Sol seque a água",
 							fundo:""
 						},
 						alternativa3:{
 							texto:"Todas as Alternativas",
 							fundo:""
 						}

 					},
 					{
 						pergunta:"Qual é o mosquito que transmite a Dengue, Chikungunya, Zica e Febre Amarela?",
 						alternativa1:{
 							texto:"Aedes Aegypti",
 							fundo:""
 						},
 						alternativa2:{
 							texto:"Aedes Albopictus",
 							fundo:""
 						},
 						alternativa3:{
 							texto:"Muriçoca",
 							fundo:"",
 						}
 					},
 					{
 						pergunta:"Qual é a doença transmitida pelo rato?", 						
 						alternativa1:{
 							texto:"Leptospirose",
 							fundo:""
 						},
 						alternativa2:{
 							texto:"Teníase",
 							fundo:""
 						},
 						alternativa3:{
 							texto:"Febre amarela",
 							fundo:""
 						}
 					},
 					{
 						pergunta:"O que representa o Outubro Rosa?", 						
 						alternativa1:{
 							texto:"Mês da mulher",
 							fundo:""
 						},
 						alternativa2:{
 							texto:"Mês em que as mulheres vãose examinar",
 							fundo:""
 						},
 						alternativa3:{
 							texto:"Mês da prevensão ao câncerde mama",
 							fundo:""
 					}
 						}
 				],
 				MeioAmbiente:[
 				{
 					pergunta:"Quanto tempo dura uma tampa de garrafa no meio ambiente?",
 					alternativa1:{
 						texto:"2 anos",
 						fundo:""
 					},
 					alternativa2:{
 						texto:"2 meses",
 						fundo:""
 					},
 					alternativa3:{
 						texto:"15 anos",
 						fundo:""
 					}

 				},
 				{
 					pergunta:"Qual é o tempo de decomposição da garrafa pet?",
 					alternativa1:{
 						texto:"10 anos",
 						fundo:""
 					},
 					alternativa2:{
 						texto:"50 meses",
 						fundo:""
 					},
 					alternativa3:{
 						texto:"500 anos",
 						fundo:""
 					}
 				},
 				{
 					pergunta:"O que devemos colocar no pratinho da planta?",
 					alternativa1:{
 						texto:"Água",
 						fundo:""

 					},
 					alternativa2:{
 						texto:"Água",
 						fundo:""
 					},
 					alternativa3:{
 						texto:"Barro",
 						fundo:""
 					}
 				},
 				{
 					pergunta:"Em quais produtos o plástico pode se transformar?",
 					alternativa1:{
 						texto:"Óleo de motor e tecido",
 						fundo:""
 					},
 					alternativa2:{
 						texto:"Mangueira Vassoura",
 						fundo:""

 					},
 					alternativa3:{
 						texto:"Todas as Alternativas",
 						fundo:""

 					}
 				}
 				]
			}
		},
		methods:{
			addmeioambiente(){
				return this.preenchimento = 'MeioAmbiente'
			},
			addsaude(){
				return

			},
			addconsumoconsciente(){

			}
			
		}
	}

</script>
<style scoped>



section {
	display: flex;
	flex-direction:column;
	color: #fff;
	background-color: #9ACD32;
	text-decoration:none;

}
li{
	text-decoration: none;
}

.barata{
	width: 25%;
	background-image: url(../assets/barata.jpg);
	background-size: 100%;
	background-repeat: no-repeat;
}
	
.todas{
	width: 25%;
	/*height: 50%;*/
ss	background-color: orange;
	background-size: 100%;
	background-repeat: no-repeat;

}
.consumo{
	width: 25%;
	background-color: orange;
}
.cuidado{
	width: 25%;
	background-color: orange;

}
.disperdicio{
	width: 25%;
	
	background-color: orange;
}
.pessoa-1{
	width: 25%;
	background-color: orange;
}
.pessoa-2{
	width: 30%;
	background-color: orange;
}
.pessoa-3{
	width: 30%;
	background-color: orange;
}

</style>
@media screen and (max-width: 320px)
