# OmnetSolutions

Repositório de solução de problemas em simulações do Veins, SUMO e OMNET++ 


## Documentação:

```
https://docs.omnetpp.org/
https://github.com/shigeya/omnetpp/tree/master/samples/tictoc
https://omnetpp.org/documentation/
https://github.com/burtonwilliamt/carlogicapi/tree/master/tutorials
https://veins.car2x.org/documentation/
https://veins.car2x.org/documentation/modules/
https://veins.car2x.org/documentation/faq/
```


## Solução de Problemas

## 1. Obstaculos não encontrados

Caso não sejam utilizados obstaculos como prédios para o sinal de rádio, as alterações seguintes devem ser feitas:

*  Arquivo config.xml:

Comentar as linhas:

```
<!-- Inicio comentario
		<AnalogueModel type="SimpleObstacleShadowing">
			<parameter name="carrierFrequency" type="double" value="5.890e+9"/>
			<obstacles>
				<type id="building" db-per-cut="9" db-per-meter="0.4" />
			</obstacles>
		</AnalogueModel>
		Fim do comentario -->
   ```
    
 * Arquivo omnetpp.ini:
    
  Comentar as linhas:
    
 ``` 
#*.obstacles.debug = false
#*.obstacles.obstacles = xmldoc("config.xml", "//AnalogueModel[@type='SimpleObstacleShadowing']/obstacles")

Fonte: https://stackoverflow.com/questions/54615901/how-to-fix-simpleobstacleshadowing-error-no-obstacles-have-been-added-in-mod
 
 ```
    


