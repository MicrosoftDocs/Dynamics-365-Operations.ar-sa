---
title: تسجيل الاشتراك في وتثبيت خدمة الفوترة الإلكترونية
description: توفر هذه المقالة معلومات عن كيفية التسجيل في خدمة الفواتير الإلكترونية وتثبيتها.
author: gionoder
ms.date: 02/07/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: gionoder
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.custom: ''
ms.assetid: ''
ms.search.form: ''
ms.openlocfilehash: 99f484e5ab8821c78fde776a9d3195dade2a09d5
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/12/2022
ms.locfileid: "9283946"
---
# <a name="sign-up-for-and-install-the-electronic-invoicing-service"></a>تسجيل الاشتراك في وتثبيت خدمة الفوترة الإلكترونية

[!include [banner](../includes/banner.md)]

توفر هذه المقالة معلومات عن كيفية التسجيل في خدمة الفواتير الإلكترونية وتثبيتها. توجد أربع خطوات لهذه العملية. الخطوات من 1 إلى 3 مطلوبه، والخطوة 4 اختياريه.

### <a name="step-1-sign-up-for-regulatory-configuration-service"></a>الخطوة 1: الاشتراك في Regulatory Configuration Service

توفر Regulatory Configuration Service (RCS) تجربة التكوين والتصميم المستخدمة في تكوين الفواتير الإلكترونية. ويتم إنشاء موارد مثل البيئات وميزات الفوترة الإلكترونية وصيانتها وإدارتها في RCS. عندما تكون الموارد جاهزة، يتم نشرها إلى خدمة الفوترة الإلكترونية.

لمزيد من المعلومات حول RCS، راجع [Regulatory Configuration Services (RCS) - ميزات العولمة](rcs-globalization-feature.md).

للاشتراك في RCS، انتقل إلى صفحة [Regulatory Configuration Service](https://marketing.configure.global.dynamics.com/).

### <a name="step-2-install-the-add-in-for-microservices-in-microsoft-dynamics-lifecycle-services"></a>الخطوة 2: تثبيت الوظيفة الإضافية للخدمات المصغرة في Microsoft Dynamics ‏Lifecycle Services

خدمة الفوترة الإلكترونية عبارة عن مجموعة من الخدمات المصغرة التي تتم استضافتها في مراكز بيانات Microsoft. بشكل افتراضي، ليس لدى عملاء Dynamics 365 Finance و Dynamics 365 Supply Chain Management حق الوصول إلى خدمة الفوترة الإلكترونية. يجب عليك تثبيتها كوظيفة اضافيه في Microsoft Dynamics Lifecycle Services (LCS). عند تثبيت الوظيفة الإضافية، يتم تسجيل بيئة Finance أو Supply Chain Management في سجل التطبيقات المسموح لها بالاتصال بخدمة الفوترة الإلكترونية.

لإكمال هذه الخطوة، راجع [تثبيت الوظيفة الإضافية للخدمات المصغرة في Lifecycle Services](e-invoicing-install-add-in-microservices-lcs.md).

### <a name="step-3-set-up-rcs"></a>الخطوة 3: إعداد RCS

يجب عليك إعداد التكامل بين RCS وخدمة الفوترة الإلكترونية. كما يجب أيضا اعداد المكونات الرئيسية.

لإكمال هذه الخطوة، راجع [إعداد Regulatory Configuration Service (RCS)](e-invoicing-set-up-rcs.md).

### <a name="step-4-microsoft-power-platform-plug-in-admin-reference"></a>الخطوة 4: مرجع إدارة المكونات الإضافية لـ Microsoft Power Platform

تتطلب بعض السيناريوهات التكامل مع Dataverse في نطاق Microsoft Power Platform.

يعد هذا الإعداد حاليًا إلزاميًا إذا كنت ستستخدم حلول الفواتير الإلكترونية لسيناريوهات الفواتير الإلكترونية الإندونيسية. ومع ذلك، فهو اختياري لسيناريوهات الفواتير الإلكترونية في المملكة العربية السعودية. لمزيد من المعلومات، راجع [توفر ميزات الفوترة الإلكترونية حسب البلد أو المنطقة](e-invoicing-country-specific-availability.md).

لإكمال هذه الخطوة، راجع [مرجع إدارة المكونات الإضافية في Microsoft Power Platform](e-invoicing-power-platform-plug-in.md).
