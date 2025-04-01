# PROJETO-4-MODELAGEM-DE-UM-PEQUENO-SISTEMA-COM-UML-E-BPMN



[INÍCIO] -> [usuário acessa o sistema] -> [seleciona sala e horário] -> [verifica disponibilidade] -> {sala disponível?} <br>
    -> [SIM] -> [reserva confirmada] -> [FIM] <br>
    -> [NÃO] -> [exibe salas alternativas] -> [FIM] <br>


+------------------------------------+<br> 			
CLIENTE<br> 							
+------------------------------------+<br>			
- NOME: STRING<br>  							               
- EMAIL: STRING<br>  						               			   		
+------------------------------------+<br>							
	+ REALIZARPEDIDO()<br>					            	
+------------------------------------+ <br>      
CLIENTE 1===0 (FALSE)<br>                          
CLIENTE 1===1 (TRUE)<br>                    
<br>
<br>
+------------------------------------+<br>
PEDIDO<br>
+------------------------------------+<br>
- DATA: DATE<br>
- STATUS: STRING<br>
+------------------------------------+<br>
- CONFIRMAR()<br>
<br>
<br>
+------------------------------------+<br>			
SALA<br>
+------------------------------------+<br>			
- LUGAR: STRING	<br>							
- BLOCO: STRING<br>
- DATA: STRING<br>
- DISPONÍVEL: STRING<br>				  		
+------------------------------------+								
	+ RESERVAR LUGAR<br>							
+------------------------------------+<br>				
RESERVA 1===0(FALSE)<br>
RESERVA 1===1(TRUE) -> [REMOVIDO DA LISTA DE RESERVAS]<br>
<br>
<br>
