---
title: "تكوين ومعالجة عملية استبدال في أمر إرجاع"
description: "يشرح هذا الموضوع كيفية تكوين عملية استبدال في أمر إرجاع في Microsoft Dynamics 365 for Retail."
author: josaw1
manager: AnnBe
ms.date: 11/12/2018
ms.topic: index-page
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2018-11-15
ms.dyn365.ops.version: 
ms.translationtype: HT
ms.sourcegitcommit: 3331b984693c58c6ee8c49b98ed7d3a8df5b79ff
ms.openlocfilehash: 45b628376a483d3d639e5c018dd93570ed8ce7af
ms.contentlocale: ar-sa
ms.lasthandoff: 12/04/2018

---
# <a name="configure-and-process-an-exchange-on-a-return-order"></a>تكوين ومعالجة عملية استبدال في أمر إرجاع

[!include [banner](includes/banner.md)]

في الإصدارات السابقة من Microsoft Dynamics 365 for Retail، كانت معالجة المرتجعات في مقابل أوامر العملاء تتم باستخدام مستند أمر الإرجاع في Retail Headquarters. ومع ذلك، يمكن استخدام مستند أمر الإرجاع لمعالجة المنتجات المرتجعة فقط. يُشار إلى المنتجات المرتجعة بكمية سالبة في بنود أمر الإرجاع. وبطريقة مغايرة، يُشار إلى المبيعات بكمية موجبة. ومع ذلك، لا يدعم مستند أمر الإرجاع الكميات الموجبة. وبسبب هذا القيد، لم تدعم الإصدارات السابقة من Retail السيناريوهات حيث كانت عمليات الاستبدال تتم فقط باستخدام مستند أمر الإرجاع.

ومع ذلك، تمت إضافة وظيفة لدعم السيناريوهات حيث تتم عمليات الاستبدال على الأوامر المرتجعة. يستخدم Retail الآن مستند أمر المبيعات بدلاً من مستند أمر الإرجاع لمعالجة هذه الأنواع من الحركات.

## <a name="configure-retail-to-support-exchanges-on-return-orders"></a>تكوين Retail لدعم عمليات الاستبدال على أوامر الإرجاع

اتبع هذه الخطوات لتكوين النظام لدعم عمليات الاستبدال على أوامر الإرجاع.

1. انتقل إلى **البيع بالتجزئة \> إعداد Headquarters \> المعلمات \> معلمات البيع بالتجزئة**. على علامة التبويب السريعة **أوامر العملاء‬**، عيّن الخيار **معالجة أوامر الإرجاع كأوامر مبيعات** إلى **نعم**.
2. شغّل وظيفة **جدول توزيع التكوين العمومي** (**1110**).

## <a name="make-an-exchange"></a>إجراء عملية استبدال

بعد أن يتم تكوين النظام كما ورد في المقطع السابق، سيحدد مستخدم نقطة البيع (POS) أمر مبيعات أو فاتورة مبيعات لمعالجة عملية إرجاع، كما هو الحال في إصدارات Retail السابقة. ومع ذلك، بعد إضافة الأصناف المرتجعة إلى سلة التسوق، سيتمكن المستخدم من إضافة بنود مبيعات جديدة إلى سلة التسوق.

بالنسبة إلى بنود المبيعات الجديدة هذه، يجب على المستخدم تحديد كافة السمات المطلوبة لمعالجة بند في أمر العميل. تتضمن هذه السمات أسلوب التسليم وموقع التنفيذ. سيكون الدفع المستحق للحركة عبارة عن قيمة صافية لبنود أمر الإرجاع وبنود أمر المبيعات. عند تقديم الدفع للحركة، سيتم ترحيل أمر الإرجاع كمستند أمر مبيعات في Retail Headquarters، وسيقوم النظام بفوترة بنود الإرجاع على الفور.

لتوفير رؤية أفضل لمختلف المبالغ في سلة التسوق، تمت إضافة ثلاثة حقول مبالغ جديدة إلى سلة التسوق. ويمكنك استخدام مصمم الشاشة لجعل كافة هذه الحقول الجديدة متوفرة في واجهة مستخدم (UI) نقطة البيع.

- **‏‫تم استخدام الإيداع‬** – مبلغ الإيداع المطبق على حركة عندما يقوم المستخدم بانتقاء أمر العميل‬. إذا لم يكن هناك أي مبلغ تجاوز الإيداع، وإذا تم تكوين إيداع بنسبة 10 بالمئة، سيكون المبلغ في هذا الحقل 90 بالمئة من المبلغ الإجمالي لأمر العميل.
- **تنفيذ المبلغ** – المبلغ الإجمالي للبنود حيث تم تعيين وضع التسليم إلى **تنفيذ** عندما تم إنشاء أمر العميل أو تحريره، أو خلال استبدال أمر العميل. يتضمن المبلغ الموجود في هذا الحقل الضرائب والمصاريف.
- **المبلغ المرتجع‬** – المبلغ الإجمالي للبنود ذات الكميات السالبة أثناء استبدال أمر العميل. يتضمن المبلغ الموجود في هذا الحقل الضرائب والمصاريف.
