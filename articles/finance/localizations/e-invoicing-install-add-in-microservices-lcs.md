---
title: تثبيت الوظيفة الإضافية للخدمات المصغرة في Lifecycle Services
description: تشرح هذه المقالة كيفية تثبيت الوظيفة الإضافية الفوترة الإلكترونية في Microsoft Dynamics ‏Lifecycle Services ‏(LCS).
author: gionoder
ms.date: 02/11/2022
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
ms.openlocfilehash: 938b00192acc0ff5534239f2f280792471181fad
ms.sourcegitcommit: 1ecfc1d8afb2201ab895ae6f93304ba2b120f14b
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/21/2022
ms.locfileid: "9710798"
---
# <a name="install-the-add-in-for-microservices-in-lifecycle-services"></a>تثبيت الوظيفة الإضافية للخدمات المصغرة في Lifecycle Services

[!include [banner](../includes/banner.md)]

تتطلب المصادقة في خدمة الفوترة الإلكترونية أن تقوم بتسجيل بيئة Microsoft Dynamics 365‎ Finance أو Dynamics 365 Supply Chain Management في النظام الأساسي للخدمات عن طريق تثبيت الوظيفة الإضافية لبيئتك في Microsoft Dynamics ‏Lifecycle Services ‏(LCS).

لتسجيل بيئة، اتبع هذه الخطوات.

1. سجل دخولك إلى حساب LCS.
2. في لوحة المشروع، حدد مشروع LCS.
2. في المشروع، على لوحة معلومات **البيئة**، حدد البيئة المنشورة لك. يجب أن تكون البيئة التي تحددها قيد التشغيل.
3. في علامة التبويب **تكامل Power Platform**، في قسم **الوظائف الإضافية للبيئة**، حدد **تثبيت وظيفة إضافية جديدة**.
4. حدد **الفوترة الإلكترونية**.
5. في الحقل **معرف التطبيق AAD**، أدخل القيمة الثابتة **091c98b0-a1c9-4b02-b62c-7753395ccabe**. تكون هذه القيمة ثابتة دائماً. تاكد من إدخال معرف فريد عمومي (GUID) فقط. لا تقم بتضمين إيه رموز أخرى، مثل المسافات أو الفاصلات أو النقاط أو علامات الاقتباس.
6. في الحقل **معرف مستأجر AAD**، أدخل معرف المستأجر لحساب اشتراك Azure. يجب أن يكون مستأجر Azure Active Directory (Azure AD) الذي تحدده هو نفس المستأجر المستخدم لـ Regulatory Configuration Service (RCS).
7. راجع البنود والشروط، ثم حدد خانة الاختيار.
8. حدد **تثبيت**. بعد بضع دقائق، يجب أن تغير الحالة من **قيد التثبيت** إلى **مثبت**. قد تحتاج إلى تحديث الصفحة لعرض هذا التغيير.

الفوترة الكترونيه جاهزه الآن للاستخدام.

> [!NOTE]
> عادة ما يكون لدى الشركات العديد من بيئات Finance أو Supply Chain Management. تتضمن هذه البيئات بيئات الإنتاج وبيئات اختبار قبول المستخدم (UAT) وبيئات التطوير (وضع الحماية). يجب عليك إكمال الإجراء السابق لجميع البيئات التي تريد ربطها بالفوترة الإلكترونية.
