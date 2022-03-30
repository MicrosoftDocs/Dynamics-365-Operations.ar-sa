---
title: إزالة تثبيت حلول تنسيق تطبيق الكتابة المزدوجة
description: يصف هذا الموضوع كيفيه إزالة تثبيت حلول تنسيق تطبيق الكتابة المزدوجة.
author: RamaKrishnamoorthy
ms.date: 03/16/2022
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2022-01-21
ms.openlocfilehash: 781b2cb19a563d5712fa65718c93bfdc242f0c4a
ms.sourcegitcommit: abfaef124c8747827d6f297821f01f1f6fbca6b7
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/17/2022
ms.locfileid: "8455314"
---
# <a name="uninstall-dual-write-application-orchestration-solutions"></a>إزالة تثبيت حلول تنسيق تطبيق الكتابة المزدوجة

[!include [banner](../../includes/banner.md)]

يصف هذا الموضوع كيفيه إزالة تثبيت حلول تنسيق تطبيق الكتابة المزدوجة.

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
