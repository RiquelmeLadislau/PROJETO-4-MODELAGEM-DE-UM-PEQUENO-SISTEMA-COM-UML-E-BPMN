# PROJETO-4-MODELAGEM-DE-UM-PEQUENO-SISTEMA-COM-UML-E-BPMN



[USUÁRIO] ------------> [ATENDENTE]
    ---> (FAZ O PEDIDO)   ---> (RECEBE O PEDIDO) ---> (VERIFICA SALAS DISPONÍVEIS)
                                                                  ---> (SIM)
                                                                        ---> (RESERVA DATA/HORA/DIA)
                                                                  ---> (NÃO)
                                                                        ---> (RETORNA PARA O USUÁRIO)




+------------------------------------+				+------------------------------------+
CLIENTE									                       PEDIDO
+------------------------------------+				+------------------------------------+
- NOME: STRING								                -DATA: DATE
- EMAIL: STRING								                - STATUS: STRING			   		
+------------------------------------+				+------------------------------------+					
	+ REALIZARPEDIDO()					                 + CONFIRMAR()		
+------------------------------------+        +------------------------------------+
CLIENTE 1===0 (FALSE)                          RESERVA 1 === 0(FALSE) [ESPAÇO JÁ AGENDADO, PORFAVOR VOLTE OUTRO DIA!]
CLIENTE 1===1 (TRUE)	                         RESERVA 1 === 1(TRUE) [RESERVA]


+------------------------------------+				
SALA
+------------------------------------+				
- LUGAR: STRING								
- BLOCO: STRING
- DATA: STRING
- DISPONÍVEL: STRING				  		
+------------------------------------+								
	+ RESERVAR LUGAR							
+------------------------------------+					
RESERVA 1===0(FALSE)
RESERVA 1===1(TRUE) -> [REMOVIDO DA LISTA DE RESERVAS]
