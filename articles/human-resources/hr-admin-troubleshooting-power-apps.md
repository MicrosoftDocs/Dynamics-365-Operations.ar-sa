---
title: لا يمكن إنشاء بيئة في مركز إدارة Power Apps
description: يشرح هذا المقال الخطوات التي يجب اتخاذها إذا تعذر على المسؤول إنشاء بيئة في مركز إدارة Microsoft Power Apps.
author: twheeloc
ms.date: 08/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: cc62d3c8fe560d4f7d2e754a79de6fec3ef6041b
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/03/2022
ms.locfileid: "8882913"
---
# <a name="cant-create-an-environment-in-the-power-apps-admin-center"></a>لا يمكن إنشاء بيئة في مركز إدارة Power Apps


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

**إصدار**

- يتعذر على مسؤول المستأجر/البيئة إنشاء بيئة في مركز إدارة Microsoft Power Apps.
- لا يمتلك المستخدم ترخيصًا يمنح الحق في إنشاء البيئات.

**الحل**

تأكد من أن مسؤول المستأجر قد قام بتعيين ترخيص Power Apps P2 صالح للمستخدم الذي يقوم بإنشاء البيئة. توفر خطة خدمة Microsoft Dynamics التالية أذونات لإنشاء بيئات:

| وحدة حفظ مخزون المنتج الكلي (SKU)       | خطة خدمة Power Apps P2  |
|------------------------------------------------|----------------------------|
| Microsoft Dynamics 365 for Operations          | Power Apps لـ Dynamics 365 |
| خطة Microsoft Dynamics 365، Enterprise Edition | Power Apps لـ Dynamics 365 |

لاحظ أن وحدات Microsoft Office المختلفة توفر الحق أيضًا، بالإضافة إلى وحدات SKU المستقلة للخطة 2 من Power Apps. النقطة المهمة هي وجود إحدى وحدات SKU.

1. الانتقال إلى [https://preview.admin.powerapps.com/environments](https://preview.admin.powerapps.com/environments).
2. إنشاء البيئات باتباع الإرشادات الموجودة في [توفير Human Resources](/dynamics365/unified-operations/talent/provisioning-talent).


[!INCLUDE[footer-include](../includes/footer-banner.md)]
