# INF331-2020

**Rodrigo Yokoo Siqueira Bueno**

# Tarefa sobre catálogo de componentes
## Arquivo do Notebook
[components-01-catalog.ipynb](notebook/components-01-catalog.ipynb)

# Tarefa Web Components 1

	<dcc-trigger label="Mundo"
				 action="noticia/mundo/politica"
				 value="Explosão em Beirute">
	</dcc-trigger>
	<dcc-trigger label="Brasil P"
				 action="noticia/brasil/politica"
				 value="Bolsonaro pegou Covid-19">
	</dcc-trigger>
	<dcc-trigger label="Brasil E"
				 action="noticia/brasil/esporte"
				 value="Corinthias é campeão paulista de 2020">
	</dcc-trigger>
	<dcc-trigger label="Bahia"
				 action="noticia/bahia/esporte"
				 value="Campeonato bahiano suspenso novamente.">
	</dcc-trigger>
	<dcc-lively-talk id="doctor"
					 duration="0s"
					 character="doctor"
					 speech="Hello, ">
	  <subscribe-dcc topic="noticia/+/politica"></subscribe-dcc>
	</dcc-lively-talk>
	<dcc-lively-talk id="nurse"
					 duration="0s"
					 character="nurse"
					 speech="Hello, ">
	  <subscribe-dcc topic="noticia/brasil/#"></subscribe-dcc>
	</dcc-lively-talk>
	<dcc-lively-talk id="patient"
					 duration="0s"
					 character="patient"
					 speech="Hello, ">
	  <subscribe-dcc topic="noticia/#"></subscribe-dcc>
	</dcc-lively-talk>




# Tarefa Web Components 2
	<dcc-trigger label="Next Item" action="next/rss">
	</dcc-trigger>

	<dcc-rss publish="rss/science" source="https://www.wired.com/category/science/feed">
	  <subscribe-dcc topic="next/rss" role="step"></subscribe-dcc>
	</dcc-rss>

	<dcc-rss publish="rss/design" source="https://www.wired.com/category/design/feed">
	  <subscribe-dcc topic="next/rss" role="step"></subscribe-dcc>
	</dcc-rss>

	<dcc-aggregator publish="aggregate/science" quantity="3">
	  <subscribe-dcc topic="rss/science"></subscribe-dcc>
	</dcc-aggregator>

	<dcc-lively-talk id="doctor"
					 duration="0s"
					 character="doctor"
					 speech="">
	  <subscribe-dcc topic="aggregate/science"></subscribe-dcc>
	</dcc-lively-talk>

	<dcc-lively-talk id="nurse"
					 duration="0s"
					 character="nurse"
					 speech="">
	  <subscribe-dcc topic="rss/science"></subscribe-dcc>
	</dcc-lively-talk>

	<dcc-lively-talk id="patient"
					 duration="0s"
					 character="patient"
					 speech="">
	  <subscribe-dcc topic="rss/design"></subscribe-dcc>
	</dcc-lively-talk>

