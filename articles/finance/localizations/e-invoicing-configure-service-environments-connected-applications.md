---
title: تكوين بيئات الخدمات والتطبيقات المتصلة
description: توفر هذه المقالة معلومات عن كيفية تكوين بيئات الخدمة والتطبيقات المتصلة.
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
ms.openlocfilehash: c1bb3f784148f04c01223ac4e280a18bacfe0e51
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/03/2022
ms.locfileid: "8853211"
---
# <a name="configure-service-environments-and-connected-applications"></a>تكوين بيئات الخدمات والتطبيقات المتصلة

[!include [banner](../includes/banner.md)]

توفر هذه المقالة معلومات عن كيفية تكوين بيئات الخدمة والتطبيقات المتصلة. توجد ثلاث خطوات لهذه العملية. الخطوة 1 إلزاميه، والخطوتان 2 و 3 اختياريه.

## <a name="step-1-create-a-service-environment"></a>الخطوة 1: إنشاء بيئة خدمة

عندما تقوم بإنشاء بيئة الخدمة الخاصة بك، حدد قائمه المستخدمين الذين يمكنهم نشر ميزات العولمة اليه. بشكل اختياري، بالنسبة لبعض وحدات السيناريو، حدد قائمه التطبيقات الخارجية التي يمكنها الاتصال بخدمه الفوترة الكترونيه. قم باعداد التسلسلات الرقمية إذا كنت ستستخدمها في وحدات السيناريو الخاصة بك.

لإكمال هذه الخطوة، راجع [بيئات الخدمة](e-invoicing-service-environments.md).

## <a name="step-2-add-certificates-and-secrets"></a>الخطوة 2: شهادات العملاء وأسرارهم

أضف مرجعًا إلى المخزن الرئيسي في Microsoft Azure والأسرار لاستخدامها في السيناريوهات الخاصة بك. تكون هذه الخطوة إلزاميه إذا كانت الإجراءات الموجودة في أنابيب المعالجة تستخدم الشهادات والاسرار للتوقيع الرقمي أو الاتصال بخدمات الويب الخارجية.

لإكمال هذه الخطوة، راجع [شهادات العملاء وأسرارهم](e-invoicing-customer-certificates-secrets.md).

## <a name="step-3-configure-connected-applications"></a>الخطوة 3: تكوين التطبيقات المتصلة

لإعداد الاتصال بين تطبيقات Dynamics 365 Finance أو Dynamics 365 Supply Chain Management والفوترة الإلكترونية، يجب عليك تكوين Supply Chain Management لإنشاء الاتصال بخدمة الفوترة الإلكترونية وإعداد بيانات الأعمال في هيكل موحد يمكن تحويله إلى التنسيق الإلكتروني المطلوب. يجب على التطبيقات أيضًا معالجة الاستجابات من الخدمة بشكل صحيح. يمكنك إكمال هذا التكوين مباشرةً في بيئة Finance أو Supply Chain Management، أو يمكنك إكمالها في Regulatory Configuration Service (RCS). إذا أكملت التكوين في RCS، يمكنك بعد ذلك نشره في بيئة Finance أو Supply Chain Management الخاصة بك. في هذه الخطوة، ستقوم بتسجيل التطبيق المتصل لنشر المعلمة.

لإكمال هذه الخطوة، راجع [التطبيقات المتصلة](e-invoicing-connected-applications.md).
