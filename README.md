# HEALTH DATA INTELLIGENCE & OWNERSHIP CONSORTIUM (HDIOC)  



## ARCHITECTURE  

<img src="" width="100%" >

## OBJECTIVE  

HEALTH DATA INTELLIGENCE & OWNERSHIP CONSORTIUM (HDIOC) is a Consortium of Hospitals who is given access to latest technologies for getting insights and conclusions regarding the patients health and agree up on certain rules and regulations to make sure the entire process of handling Health related data and records of the patient can be done in such a way that the patient has entire ownership and control over their data.  


## PROBLEMS  

* People consult with multiple hospitals and doctors for the same health issue  
* Many hospitals follow a system where any health data they collect as part of a patient's medical treatment is kept in their database and only a token or card that references to this data is handed over to the patient.  
* Patients often find it very difficult to have access to all this data when they change their health care provider.  
* Patients do not have any control on who has access to their data.  
* Doctors often start with test doses of medicines due to lack of access to proper insights and analytics into the health conditions of their patient  
* There are no specific terms and conditions set up on what the hospital can do with the health data collected from patients.  
* Doctors often do not get an entire picture of their patient in cases where parts of the data lie with a different health care provider.  
* Health insurance providers face difficulties in authenticating the data and processing the insurance and are often time consuming.  
* All hospitals may not have all the medical equipment and often needs some tests to be taken from other hospitals.  


## EXPECTED OUTCOMES  

* Patients should be able to list any health data collected about them at any instant of time in their portal and should have the option to authorise or unauthorize any entities from having access to their data.  
* Analysis and Predictions about the health of the patient should be available to the doctor based on the authorised data provided by the patient.  
* Health insurance providers must be able to process the insurance seamlessly in no time.  
* Doctors should be able to submit their conclusion and analysis about a patient and be able to request for access to past health records to the user.  
* Hospitals or any Health Care service providers should be able to share the data in between them in a well trusted manner provided it's authorised by the patient.  


## IMPLEMENTATION  

A Dashboard will be created that can be used for the patients, doctors and health insurers to satisfy their requirements. App engine will be used to run this web app. The web app will be built using NodeJs. Hyperledger fabric blockchain which is a permissioned blockchain network will be used for creating the consortium of multiple hospitals. Each hospital that agrees on the terms and conditions of the consortium network are called as the “members”. They are required to set up their peers with appropriate cryptographic materials like Certificate authority for participating in the network. The entire process of adding a new hospital to the network will be streamlined via the web app. The patients, doctors and health insurers can separately register with the network via the web app by providing and verifying the necessary information. Once all the entities in the process are registered with the platform, the client application can broadcast the transaction request to the network. Endorser peers present in each member will check for the certificate details and validate the transaction. The peers sents the transaction approval or rejection response. The client sends approved transactions to the Orderer peer so that it gets properly ordered and included to the blockchain and forwards the transaction block to anchor nodes of different members in the network. Then Anchor nodes broadcast it to other peers inside the hospital and update their local ledger. Storing files like images, scan reports and other health related data of the users is handled by making use of cryptographic hash functions, so that the data can be stored off chain and a verifiable proof that the image or any specific file which was hashed at the time transaction was recorded on the blockchain can be linked to a url containing the hash which can be kept on chain. The hash that acts as a reference to the data will be used in further transactions. The medical records and other health related data uploaded by each hospital undergo the hashing process and hash in referenced and stored inside the blockchain. The data which could be images, Electronic Health Records, etc which will get stored in Cloud file storage. The Cloud Healthcare API provides an easy and standardised data exchange and storage between the healthcare applications and solutions. For further processing, analytics and other machine learning capabilities the output data will be processed upon by Dataproc and Datastream, and can be stored in Bigquery for scalable analytics and machine learning model training will be done with Vertex AI. Doctors will be able to get access to this to the analytics, inference and predictions from the machine learning models created on top of the patients data, thus allowing them to provide the most efficient medications and treatments for their patients based on the authorised and authenticated data provided by the patients. In the entire workflow the patients get to control and see the information regarding which all members possess their health related data and for what all purposes each member is using their data.  


# APPLICATION  

* Efficient medication and treatment can be provided by the doctors by making use of authenticated and authorised data available about the patient.  
* The patient becomes aware about who has access to his related data and for what purposes it's being used and gets to choose who can access their data.  
* The seamless availability of data across hospitals from a single platform makes sure there is no time delay or difficulties faced by patients in handling their data across multiple providers.  
* The Health Insurance gets processed seamlessly since the authenticated data by doctors and patients with proper records on the blockchain is available.  


# PLANNING  

* A Dashboard will be created which provides a dashboard for patients, doctors and health
* insurance providers and will be run on App Engine.
* A Blockchain network will be set up by making use of the Hyperledger Fabric and Composer with an initial network having three hospitals.
* The additional compute requirements as well as api endpoint creation will be done using cloud run and cloud functions
* A data movement implementation from client hospitals and patients to the off chain storage with proper hashing will be set up.
* The data analytics pipelines with the data from Cloud storage and Cloud Healthcare API will be set up using DataProc, Dataflow and BigQuery, with ML model creation using Vertex AI.








