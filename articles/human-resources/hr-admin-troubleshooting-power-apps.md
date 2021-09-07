---
title: لا يمكن إنشاء بيئة في مركز إدارة Power Apps
description: يشرح هذا الموضوع الخطوات التي يجب اتخاذها إذا تعذر على المسؤول إنشاء بيئة في مركز إدارة Microsoft Power Apps.
author: twheeloc
ms.date: 08/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 50a5aac71ec8ed850cfad32bdb1b8d589eb2885a
ms.sourcegitcommit: 7e32e5e39e762a4b1606161cb603a450d13b5251
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/23/2021
ms.locfileid: "7413551"
---
# <a name="cant-create-an-environment-in-the-power-apps-admin-center"></a>لا يمكن إنشاء بيئة في مركز إدارة Power Apps

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
