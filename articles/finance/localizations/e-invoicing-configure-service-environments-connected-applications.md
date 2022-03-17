---
title: تكوين بيئات الخدمات والتطبيقات المتصلة
description: يوفر هذا الموضوع معلومات حول كيفيه تكوين بيئات الخدمة والتطبيقات المتصلة.
author: dkalyuzh
ms.date: 02/09/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom:
- "97423"
- intro-internal
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: c3366e75b4a6d3f33a1aac9e444236d9ae57c829
ms.sourcegitcommit: ffdb6794746ffe5461f9dcf34ed8e64976d22d2d
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/02/2022
ms.locfileid: "8371472"
---
# <a name="configure-service-environments-and-connected-applications"></a>تكوين بيئات الخدمات والتطبيقات المتصلة

[!include [banner](../includes/banner.md)]

يوفر هذا الموضوع معلومات حول كيفيه تكوين بيئات الخدمة والتطبيقات المتصلة. توجد ثلاث خطوات لهذه العملية. الخطوة 1 إلزاميه، والخطوتان 2 و 3 اختياريه.

## <a name="step-1-create-a-service-environment"></a>الخطوة 1: إنشاء بيئة خدمة

عندما تقوم بإنشاء بيئة الخدمة الخاصة بك، حدد قائمه المستخدمين الذين يمكنهم نشر ميزات العولمة اليه. بشكل اختياري، بالنسبة لبعض وحدات السيناريو، حدد قائمه التطبيقات الخارجية التي يمكنها الاتصال بخدمه الفوترة الكترونيه. قم باعداد التسلسلات الرقمية إذا كنت ستستخدمها في وحدات السيناريو الخاصة بك.

لإكمال هذه الخطوة، راجع [بيئات الخدمة](e-invoicing-service-environments.md).

## <a name="step-2-add-certificates-and-secrets"></a>الخطوة 2: شهادات العملاء وأسرارهم

أضف مرجعًا إلى المخزن الرئيسي في Microsoft Azure والأسرار لاستخدامها في السيناريوهات الخاصة بك. تكون هذه الخطوة إلزاميه إذا كانت الإجراءات الموجودة في أنابيب المعالجة تستخدم الشهادات والاسرار للتوقيع الرقمي أو الاتصال بخدمات الويب الخارجية.

لإكمال هذه الخطوة، راجع [شهادات العملاء وأسرارهم](e-invoicing-customer-certificates-secrets.md).

## <a name="step-3-configure-connected-applications"></a>الخطوة 3: تكوين التطبيقات المتصلة

لإعداد الاتصال بين تطبيقات Dynamics 365 Finance أو Dynamics 365 Supply Chain Management والفوترة الإلكترونية، يجب عليك تكوين Finance أو Supply Chain Management لإنشاء الاتصال بخدمة الفواتير الإلكترونية وإعداد بيانات الأعمال في هيكل موحد يمكن تحويله إلى التنسيق الإلكتروني المطلوب. يجب على التطبيقات أيضًا معالجة الاستجابات من الخدمة بشكل صحيح. يمكنك إكمال هذا التكوين مباشرةً في بيئة Finance أو Supply Chain Management، أو يمكنك إكمالها في Regulatory Configuration Service (RCS). إذا أكملت التكوين في RCS، يمكنك بعد ذلك نشره في بيئة Finance أو Supply Chain Management الخاصة بك. في هذه الخطوة، ستقوم بتسجيل التطبيق المتصل لنشر المعلمة.

لإكمال هذه الخطوة، راجع [التطبيقات المتصلة](e-invoicing-connected-applications.md).
