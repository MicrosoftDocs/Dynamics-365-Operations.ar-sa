---
title: تعذر إنشاء بيئة في مركز إدارة PowerApps
description: يشرح هذا الموضوع الخطوات التي يجب اتخاذها إذا تعذر على المسؤول إنشاء بيئة في مركز إدارة Microsoft PowerApps.
author: andreabichsel
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 96119ca869cbbb15ed8d8d5d0fe3b0f94b5f36cc
ms.sourcegitcommit: 45f8cea6ac75bd2f4187380546a201c056072c59
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 07/12/2019
ms.locfileid: "1742832"
---
# <a name="cant-create-an-environment-in-the-powerapps-admin-center"></a>لا يمكن إنشاء بيئة في مركز إدارة PowerApps

[!include [banner](includes/banner.md)]

**المشكلة**

- يتعذر على مسؤول المستأجر/البيئة إنشاء بيئة في مركز إدارة Microsoft PowerApps.
- لم يتم تعيين ترخيص يمنح المستخدمين حق تنفيذ خطوة إنشاء البيئة مباشرة إلى المستخدم الذي يقوم بتنفيذ هذه الخطوة.

**الحل**

تأكد من قيام مسؤول المستأجر بتعيين ترخيص PowerApps P2 صالح مباشرة إلى المستخدم الذي سوف يقوم بتنفيذ خطوة إنشاء البيئة. فيما يلي خطط خدمة Microsoft Dynamics التي توفر هذا الحق.

| وحدة حفظ مخزون المنتج الكلي (SKU)       | خطة خدمة PowerApps P2  |
|------------------------------------------------|----------------------------|
| Microsoft Dynamics 365 for Operations          | PowerApps لـ Dynamics 365 |
| خطة Microsoft Dynamics 365، Enterprise Edition | PowerApps لـ Dynamics 365 |

لاحظ أن وحدات Microsoft Office SKU مختلفة توفر الحق أيضًا، بالإضافة إلى وحدات SKU مستقلة الخطة 2 من PowerApps. النقطة المهمة هي وجود إحدى وحدات SKU.

1. الانتقال إلى [https://preview.admin.powerapps.com/environments](https://preview.admin.powerapps.com/environments).
2. إنشاء البيئات باتباع الإرشادات الموجودة في [توفير Talent](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent).
