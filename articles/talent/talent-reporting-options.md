---
title: خيارات إعداد التقارير في Talent
description: يتناول هذا الموضوع كيفية حل المشكلة التي يريد فيها العميل تخصيص تقارير Dynamics 365 for Talent أو إنشاء تقارير جديدة.
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
ms.openlocfilehash: 8e7348a515b08523c15aa8f74d5616a3daf645b7
ms.sourcegitcommit: 45f8cea6ac75bd2f4187380546a201c056072c59
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 07/12/2019
ms.locfileid: "1741788"
---
# <a name="reporting-options-in-talent"></a>خيارات إعداد التقارير في Talent

[!include [banner](includes/banner.md)]

**تفاصيل البيئة**

تنطبق هذه المشكلة على كافة البيئات.

**العَرَضْ**

يُريد العميل تخصيص تقارير Dynamics 365 for Talent أو إنشاء تقارير جديدة.

**إصدار**

يتعذر على المستخدم تخصيص تقارير Microsoft Power BI المضمنة.

**الحل**

- يمكن الإبلاغ عن بيانات Core HR التي تتدفق إلى Common Data Service عبر موصل PowerApps Common Data Service إلى Power BI Desktop. لاحظ أن Common Data Service تحتوي على مجموعة فرعية من بيانات Core HR. لمزيد من المعلومات حول Power BI ولوحات المعلومات، راجع [إنشاء تقارير ولوحات معلومات Power BI باستخدام PowerApps Common Data Service](https://powerapps.microsoft.com/blog/cdsconnectortopowerbi).
- يتوفر إعداد التقارير الإلكترونية (ER) لبعض التقارير في Talent. يمكن إجراء التخصيصات القائمة على العميل من خلال خيارات تكوين ER.
- يمكن تصدير البيانات إلى Microsoft Excel أو Microsoft Word باستخدام كيانات البيانات المختلفة التي يوفرها Talent من خلال تكامل Microsoft Office.

**حل طويل الأجل**

ستتوفر خيارات Power BI إضافية، وسيصبح المزيد من البيانات والكيانات جزءًا من Common Data Service.
