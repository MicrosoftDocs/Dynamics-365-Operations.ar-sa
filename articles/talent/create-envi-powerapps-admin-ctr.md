---
title: "تعذر إنشاء بيئة في مركز إدارة PowerApps"
description: "يوضح هذا المقاول ما يجب عليك القيام به إذا تعذر على المسؤول إنشاء بيئة في مركز إدارة Microsoft PowerApps."
author: Darinkramer
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.translationtype: HT
ms.sourcegitcommit: d3f974f94b6c327fd70b8098d24f9e1f1e1e8eeb
ms.openlocfilehash: 6f9b7ceef6895b295e6ae5a50d8ac7970497efe5
ms.contentlocale: ar-sa
ms.lasthandoff: 12/04/2018

---

# <a name="cant-create-an-environment-in-the-powerapps-admin-center"></a>تعذر إنشاء بيئة في مركز إدارة PowerApps

[!include [banner](includes/banner.md)]

**المشكلة**

- يتعذر على مسؤول المستأجر/البيئة إنشاء بيئة في مركز إدارة Microsoft PowerApps.
- لم يتم تعيين ترخيص يمنح المستخدمين حق تنفيذ خطوة إنشاء البيئة مباشرة إلى المستخدم الذي يقوم بتنفيذ هذه الخطوة.

**الحل**

تأكد من قيام مسؤول المستأجر بتعيين ترخيص PowerApps P2 صالح مباشرة إلى المستخدم الذي سوف يقوم بتنفيذ خطوة إنشاء البيئة. فيما يلي خطط خدمة Microsoft Dynamics التي توفر هذا الحق.

| وحدة حفظ مخزون المنتج الكلي (SKU)       | خطة خدمة PowerApps P2  |
|------------------------------------------------|----------------------------|
| Microsoft Dynamics 365 for Operations          | PowerApps لـ Dynamics 365 |
| خطة Microsoft Dynamics 365 - Enterprise Edition | PowerApps لـ Dynamics 365 |

لاحظ أن وحدات Microsoft Office SKU توفر الحق أيضًا، بالإضافة إلى وحدات SKU من PowerApps خطة 2 المستقلة. النقطة المهمة هي وجود إحدى وحدات SKU.

1. الانتقال إلى [https://preview.admin.powerapps.com/environments](https://preview.admin.powerapps.com/environments).
2. إنشاء البيئات باتباع الإرشادات الموجودة في [توفير Talent](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/provisioning-talent).

