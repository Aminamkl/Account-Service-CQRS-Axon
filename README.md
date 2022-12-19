# Account-Service-CQRS-Axon
Event Sourcing et CQRS avec Spring Cloud et AXON Framework
+ L'architecture et les objectifs de ce projet : 
![image](https://user-images.githubusercontent.com/52087288/208320190-e0db6852-90ab-4abc-a737-da8e50c0e6ff.png)

# La structure du projet

![image](https://user-images.githubusercontent.com/52087288/208320273-2d60f725-01f2-4133-89ac-214a22f55515.png)

# L'exécution
## La base de données générée aprés l'éxécution
![image](https://user-images.githubusercontent.com/52087288/208320552-90ba30cf-4e38-4d3d-8e77-0bedf55a5d2c.png)

## Le test d'application
### La partie Command
+ L'ajout d'un compte

![image](https://user-images.githubusercontent.com/52087288/208320790-9531f17d-f93c-4985-a22d-0be07b4bd489.png)
![image](https://user-images.githubusercontent.com/52087288/208320820-cb8f0bd3-5fe7-4e08-bda4-9e502b45e18e.png)

+ L'affichage d'un événement par AccountID

![image](https://user-images.githubusercontent.com/52087288/208320972-f21e35c8-e245-4aea-8af3-ebe28a4e1a3b.png)

+ L'ajout d'un opération "Credit"

Le montant a crédité doit étre positif 

![image](https://user-images.githubusercontent.com/52087288/208405739-cd24e9f6-890c-4191-aa94-bc8b8b26e466.png)
![image](https://user-images.githubusercontent.com/52087288/208405885-b78cf9be-a83e-45c9-ac9a-4516165ec474.png)
![image](https://user-images.githubusercontent.com/52087288/208406003-838c6285-4ca3-48ae-b006-efdf4d03a39b.png)
![image](https://user-images.githubusercontent.com/52087288/208406450-9a44e4ea-8ec8-4fca-9efc-7a9925942f9e.png)

+ L'ajout d'un opération "Debit"

Le montant a débité doit étre positif et inférieur ou équale le montant

![image](https://user-images.githubusercontent.com/52087288/208408167-bf880284-045d-4563-ba5a-464e360e4973.png)
![image](https://user-images.githubusercontent.com/52087288/208408413-b73511b3-6581-4061-99ad-609b27af7ed3.png)
![image](https://user-images.githubusercontent.com/52087288/208408482-f43acfc0-ced6-4c12-82a3-252ff1422165.png)

+ Les opération efféctuées ont été enregistrées dans le EventStore

![image](https://user-images.githubusercontent.com/52087288/208408952-c1130d50-24ac-436c-8293-b7b95ed79cf0.png)


### La partie Query

+ L'affichage de la liste des comptes avec les opérations de chaque compte

![image](https://user-images.githubusercontent.com/52087288/208409632-31d4dcac-e97e-43bd-a527-585ffefb44f5.png)

+ L'affichage d'un compte par ID

![image](https://user-images.githubusercontent.com/52087288/208409879-91112bec-fa48-4a15-8e67-47322d816f8f.png)


