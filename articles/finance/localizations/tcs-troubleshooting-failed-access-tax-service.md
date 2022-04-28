---
title: فشل الوصول إلى خدمة الضريبة
description: يشرح هذا الموضوع كيفية استكشاف أخطاء الوصول إلى خدمة حساب الضريبة وإصلاحها.
author: hangwan
ms.date: 03/04/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: TaxIntegrationTaxServiceParameters
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: hangwan
ms.search.validFrom: 02/16/2022
ms.dyn365.ops.version: Version 10.0.21
ms.openlocfilehash: f4682b83405071b4ad7647958122ab2b4e082133
ms.sourcegitcommit: 2977e92a76211875421e608555311c363cfbdc25
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/16/2022
ms.locfileid: "8612305"
---
# <a name="failed-to-access-tax-service"></a>فشل الوصول إلى خدمة الضريبة

[!include [banner](../includes/banner.md)]


يشرح هذا الموضوع كيفية إصلاح الخطأ "فشل الوصول إلى خدمة الضرائب" في خدمة حساب الضريبة.

## <a name="symptoms"></a>العلامات

في 365 Finance Microsoft Dynamics، يمكنك الانتقال إلى **الضريبة** \> **الإعداد** \> **تكوين الضريبة** \> **معلمات خدمة الضريبة**. في علامة التبويب **عام**، يمكنك تمكين خيار **تمكين حساب الضريبة**. إذا حاولت بعد ذلك تحديد قيمة في حقل **اسم إعداد الميزة**، فسيحدث خطأ. تنص رسالة الخطأ، "فشل الوصول إلى خدمة الضرائب."

## <a name="cause"></a>السبب

يحدث هذا الخطأ لأن Finance لا يمكنه الوصول إلى خدمة حساب الضريبة.

## <a name="resolution"></a>القرار 

1. سجل دخولك إلى Microsoft Dynamics Lifecycle Services (LCS).
2. في صفحة **البيئة**، في علامة التبويب **الوظائف الإضافية للبيئة**، ابحث عن عنصر **حساب الضريبة**، وراجع حالته. الحالة يجب أن تكون **جارٍ التثبيت** أو **تم التثبيت**. إذا لم يتم تثبيت الوظيفة الإضافية لخدمة حساب الضرائب، فستتلقى الخطأ.

## <a name="mitigation"></a>تخفيف المخاطر

1. في LCS، في صفحة **Finance**، في قسم **تكامل Power Platform**، حدد **تثبيت وظيفة إضافية جديدة**.
2. قم بالتمرير لأسفل الصفحة، وحدد الوظيفة الإضافية **حساب الضريبة** لتثبيتها.
3. عد إلى بيئة Finance الخاصة بك، وحاول الوصول إلى خدمة حساب الضرائب.

> [!NOTE]
> قبل تثبيت خدمة حساب الضرائب، راجع [المتطلبات الأساسية لخدمة حساب الضريبة](global-get-started-with-tax-calculation-service.md#prerequisites).
> 
> إذا لم تتمكن من تثبيت الوظيفة الإضافية لأن قسم **تكامل Power Platform** غير متوفر، راجع [نظرة عامة على الوظيفة الإضافية](../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md). إذا استمر ظهور الخطأ بعد تثبيت الوظيفة الإضافية، فاتصل بمسؤول النظام.
