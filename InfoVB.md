# All information regarding the products that IVB is currently used

**24/9/2026**
- IVB is using **Zimperium**, **HSM**, **Centagate** from SecureMetric

1. Zimperium: started in **June 2026**, is integrated into IVB Biz+ (The banking app for corporate clients). The App is built by **React Native**
   - BundleID:
     - UAT: com.tpi.ivb.mb.biz => vn.com.indovinabank.ivbbizplusuat
     - PROD: vn.com.indovinabank.ivbbizplus
   - they using **zConsole**, **zShield**, **zDefend**, **zScan**
   - All versions that they are used:
     - zConsole: ver **5.38.3**
     - zDefend SDK **(currently)**: ver **5.8.51**. Android (App ver: **1.0.14**, App build: **0.48**). IOS (App ver: **1.0.13**. App build: **108**)
     - zDefend SDK **(Planned)**: ver **5.10.9**. Version support from Android 5.0(SDK 21) to Android 17(SDK 37) for Android. Support from IOS 12.0 to IOS 26.6 for IOS
     - zShield **(currently)**: ver **3.25.1**. Doesn't shield on IOS
     - zShield **(planned)**: ver **3.29.1**. shield on MacOS. Licensed on MacOS was granted using Mr. Khánh account. A build from TPI is expected on **September 28, 2026**. App will be shielded immediately upon availablilty
     - zScan is used for last scan in 03-Aug 2026 with Android app(v1.0.13 build 47)
    - Successfully performed the **3-month periodic review** on **September 7, 2026**
    - **Documents have been delivered**:
       - [SDK zDefend v5.10.9 for UAT](https://drive.google.com/drive/u/1/folders/1cPtiprKnfwpjDP2uT7eS-d4y3vVW6vzl)
       - [SDK zDefend v5.10.9 for Prod](https://drive.google.com/drive/u/1/folders/1cPtiprKnfwpjDP2uT7eS-d4y3vVW6vzl)
       - [zDefend-SDK-Developers-Guide-5.10.9.pdf](https://drive.google.com/drive/u/1/folders/1cPtiprKnfwpjDP2uT7eS-d4y3vVW6vzl)
       - [zDefend-SDK-Release-Notes-5.10.9.pdf](https://drive.google.com/drive/u/1/folders/1cPtiprKnfwpjDP2uT7eS-d4y3vVW6vzl)
       -  [Best Practice for threat policy](https://indovinabank-my.sharepoint.com/personal/ho_sd_indovinabank_onmicrosoft_com/_layouts/15/onedrive.aspx?id=%2Fpersonal%2Fho%5Fsd%5Findovinabank%5Fonmicrosoft%5Fcom%2FDocuments%2FZimperium%5F2026%2FZimperium%5FPROD&viewid=da59da3a%2Da281%2D461d%2Da07d%2Dbd6f1192b404&ga=1)
       -  [Mapping to State Bank of Vietnam circulars](https://indovinabank-my.sharepoint.com/personal/ho_sd_indovinabank_onmicrosoft_com/_layouts/15/onedrive.aspx?id=%2Fpersonal%2Fho%5Fsd%5Findovinabank%5Fonmicrosoft%5Fcom%2FDocuments%2FZimperium%5F2026%2FZimperium%5FPROD&viewid=da59da3a%2Da281%2D461d%2Da07d%2Dbd6f1192b404&ga=1)
       -  [Documents zimperium for IVB](https://indovinabank-my.sharepoint.com/personal/ho_sd_indovinabank_onmicrosoft_com/_layouts/15/onedrive.aspx?viewid=da59da3a%2Da281%2D461d%2Da07d%2Dbd6f1192b404&ga=1&id=%2Fpersonal%2Fho%5Fsd%5Findovinabank%5Fonmicrosoft%5Fcom%2FDocuments%2FZimperium%5F2026%2FZimperium%5FPROD%2Fdocs%2Dzimperiu%2Dfor%2DIVB%2Ezip&parent=%2Fpersonal%2Fho%5Fsd%5Findovinabank%5Fonmicrosoft%5Fcom%2FDocuments%2FZimperium%5F2026%2FZimperium%5FPROD)
       -  [Global Mobile Threat Report 2026](https://drive.google.com/file/d/1mjAwidYOTjBG3SgHtsylGKeWirG1SxJR/view?usp=sharing)
       -  [Quarterly assessment report](https://securemetrictechnology-my.sharepoint.com/my?id=%2Fpersonal%2Ftuannb%5Fsecuremetric%5Fcom%5Fvn%2FDocuments%2FAttachments%2FBao%5Fcao%5Fket%5Fqua%5Fgiam%5Fsat%5Fdinh%5Fki%5Fhe%5Fthong%5FZimperium%5FIVB%5F3%5Fthang%5Fv1%2Epdf&parent=%2Fpersonal%2Ftuannb%5Fsecuremetric%5Fcom%5Fvn%2FDocuments%2FAttachments)
    
2. Centagate
   - Overall logic Diagram:
    ![alt text][lds]
    - System components:
       - **IVB Customer**: The customer of Indovina Bank/IVB end-user
       - **Centagate Backend**: Centagate server-side software. Interacts directly with the database, executes internal system business logic, and provides APIs and integration methods
       -  **Centagate DB**: The database for the Centagate software. Centagate Db requires a MySQL or MariaDB server and can be deployed directly on the Centagate Backend server or on dedicated, standalone servers
       -  **CentagateMobileSDK**: The mobile SDK provided by SecureMetric to integrate features such as activation, OTP generation, OTP management, etc.., into IVB's Mobile Banking app
       -  **Mobile Banking App**: The bank's client-side BVSM (Mobile banking) application
       -  **Mobile Banking Backend**: The server-side Mobile Banking software that handles business logic and features provided by the Mobile Banking App. Within the scope of this project, it integrates Centagate's OTP adminstration and authentication features.
       -  **Internet Banking Backend**: The server-side Internet Banking software that processes business requirements and features provided by the internet Banking web application. Within the project's scope, it integrates Centagate's OTP authentication feature.
       -  **Operating web**: A client-side web application that handles business logic and functions provided by the Operating Web application.
       -  **Email Gateway Server**: IVB email gateway server
       -  **SMS Service**: The SMS delivery service provided by IVB
    - Physical connection diagram 
    ![alt text][dpc]

    - System status:
    ![alt text][ss]
      - IVB's production system consists of:
        - DC Site: 01 Centagate App server and 01 Database server
        - DR Site: 01 Centagate App server and 01 Database server
        - The two Database servers operate using a Master-Master replication model to ensure continuous data synchronization.
3. HSM

[lds]: logic_diagram_IVB_Cen.png "logic diagram system"
[dpc]: DC.png "DC's physical connection"
[ss]: system_structure.png "Centagate deployment model"