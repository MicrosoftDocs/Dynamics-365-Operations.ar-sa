---
title: إزالة تثبيت حلول تنسيق تطبيق الكتابة المزدوجة
description: توضح هذه المقالة كيفية إزالة تثبيت حلول تنسيق تطبيق الكتابة المزدوجة.
author: RamaKrishnamoorthy
ms.date: 03/16/2022
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2022-01-21
ms.openlocfilehash: 676802ddabac69db4947cf806e9103f67cece3de
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/03/2022
ms.locfileid: "8870363"
---
# <a name="uninstall-dual-write-application-orchestration-solutions"></a>إزالة تثبيت حلول تنسيق تطبيق الكتابة المزدوجة

[!include [banner](../../includes/banner.md)]

توضح هذه المقالة كيفية إزالة تثبيت حلول تنسيق تطبيق الكتابة المزدوجة.

يقوم بعض العملاء عن غير قصد بتثبيت حزمة تنسيق تطبيق الكتابة المزدوجة التي تقوم بتثبيت حلول متعددة في بيئتهم في Microsoft Dataverse. قد يتسبب تثبيت حلول غير ملائمة في الحزمة في حدوث مشكلات غير متوقعة وغير مرغوب فيها.

لإصلاح المشكلات المتعلقة بتثبيت حزمة تنسيق تطبيق الكتابة المزدوجة، قم بإزالة تثبيت حلول الكتابة المزدوجة غير المرغوب فيها بالترتيب التالي:

1. Dynamics365FinanceAndOperationsAnchor_managed
1. msdyn_OneFSSCM_managed (في حالة وجوده)
1. Dynamics365FinanceAndOperationsDualWriteEntityMaps_managed
1. Dynamics365Notes_managed (لإزالة تثبيت هذا الحل، يجب فتح تذكرة دعم مع Microsoft.)
1. DualWriteCore_managed
1. Dynamics365AssetManagementApp_managed
1. Dynamics365AssetManagement_managed
1. Dynamics365SupplyChainExtended_managed
1. Dynamics365FinanceExtended_managed
1. HCMCommon_managed
1. Dynamics365FinanceAndOperationsCommon_managed
1. Dynamics365Company_managed
1. CurrencyExchangeRates_managed
1. msdyn_AssetCommon_managed
1. FieldServiceCommon_managed

إذا تم تثبيت حلول دفتر العناوين العمومي والطرف، فيمكنك إزالة تثبيت الحلول بالترتيب التالي:

1. Dynamics365FinanceAndOperationsAnchor
1. Dynamics365FinanceAndOperationsDualWriteEntityMaps
1. msdyn_DualWriteCore
1. Dynamics365AssetManagementApp
1. Dynamics365AssetManagement
1. Dynamics365SupplyChainExtended
1. Dynamics365FinanceExtended
1. HCMCommon
1. Dynamics365FinanceAndOperationsCommon
1. الطرف
1. Dynamics365Company_managed
1. CurrencyExchangeRates
1. msdyn_AssetCommon
1. FieldServiceCommon
