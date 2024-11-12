---
ms.date: 11/21/2024
title: "Migrate Persistent Chat pool"
ms.reviewer: 
ms.author: serdars
author: serdarsoysal
manager: serdars
audience: ITPro
ms.topic: quickstart
ms.service: skype-for-business-server
f1.keywords:
- NOCSH
ms.localizationpriority: medium
description: "Migrate Persistent Chat pool from Skype for Business Server 2015 to Skype for Business Server 2019."
---

# Migrate Persistent Chat pool

> [!NOTE]
> If you are migrating from Skype for Business Server 2015 to Skype for Business Server 2019 and you have Persistent Chat enabled on Skype for Business Server 2015, you may encounter a situation that Chat Rooms created via Skype for Business client is not working in Skype for Business Server 2019. This is because the default Persistent Chat URL points to the previous Persistent Chat pool.

To overcome this problem, you need to move the Persistent Chat data from Skype for Business Server 2015 to Skype for Business Server 2019 and configure users appropriately. The following steps help you accomplish that:

Ensure that admin has the `RTCUniversalServerAdmins` permission assigned.

1. **Export Persistent Chat Data from Skype for Business Server 2015:**<br> 
Run the following cmdlet on the Skype for Business 2015 front-end server to export Persistent Chat data (categories, rooms, chats etc):

```powershell
Export-CsPersistentChatData -DBInstance "<backend-FQDN\instance-name>"  -FileName "C:\PersistentChatData.zip"
```
2. **Import Persistent Chat Data into Skype for Business Server 2019:**<br> 
Bring in the exported Persistent Chat data (zip file) from Skype for Business 2015 front-end server to Skype for Business 2019 front-end server. Run the following cmdlet on the Skype for Business 2019 front-end server to import Persistent Chat data:

```powershell
 Import-CsPersistentChatData -DBInstance "<backend-FQDN\instance-name>"  -FileName "C:\PersistentChatData.zip"
```

3. **Update Default Persistent Chat Pool URL in Skype for Business Server 2019:** 
    - Open the topology builder of Skype for Business Server 2019 and right-click the site-name. 
    - Select **Edit Properties** and go to the **Persistent Chat setting**. 
    - You'll notice that **Default Persistent Chat pool** has Skype for Business Server 2015 value selected in the dropdown. Change that to select Skype for Business 2019 Server pool value and select **OK**. 
    
    :::image type="content" source="../media/migration/topology-builder.png" alt-text="Screenshot of Topology builder." lightbox="../media/migration/topology-builder.png":::

    :::image type="content" source="../media/migration/edit-properties.png" alt-text="Screenshot of Edit Properties." lightbox="../media/migration/edit-properties.png":::

    - To publish the topology, select **Topology** and select **Publish**. 
       
    :::image type="content" source="../media/migration/virtual-mc-conn.png" alt-text="Screenshot of publishing topology." lightbox="../media/migration/virtual-mc-conn.png":::  
    

4. **Verify duplicate categories in Skype for Business Server 2019:**<br> 
After importing the database, ensure that duplicate categories from Skype for Business Server 2015 are created in Skype for Business Server 2019. This can be checked in the Modern Admin Control Panel(MACP). 

:::image type="content" source="../media/migration/category.png" alt-text="Screenshot of MACP." lightbox="../media/migration/category.png":::

5. **Move users from Skype for Business Server 2015 to Skype for Business Server 2019:** <br> 
Move the users from Skype for Business 2015 server to Skype for Business 2019 server using the MACP **Users** tab.

:::image type="content" source="../media/migration/admin-center-users.png" alt-text="Screenshot of MACP users." lightbox="../media/migration/admin-center-users.png":::

6. **Add users as Creators:**<br> 
Add users in the imported categories as creators. This step is necessary because the import process might not include this information.

:::image type="content" source="../media/migration/admin-center-category.png" alt-text="Screenshot of adding users as creators." lightbox="../media/migration/admin-center-category.png":::

7. **Create Persistent Chat Rooms:**<br> 
You should now be able to create Persistent Chat rooms with Skype for Business Server 2015 users having associated categories in the Skype for Business Server 2019 Persistent Chat pool or Skype for Business 2019 users in the Skype for Business 2019 Persistent Chat pool.

Additionally, if you have multiple Skype for Business 2015 Persistent Chat server pools, you need to export every database in a similar manner. Then import into Skype for Business 2019 Server and follow the steps as given above.

