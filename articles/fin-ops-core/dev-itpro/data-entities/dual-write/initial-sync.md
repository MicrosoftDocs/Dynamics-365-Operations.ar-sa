---
title: أمر التنفيذ الخاص بالمزامنة الأولية لتطبيقات Finance and Operations وCommon Data Service
description: يحدد هذا الموضوع ترتيب المزامنة الذي يجب اتباعه لإنشاء البيانات الأولية.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: befe4e12a10f4a39b90bcb4faba6431a063a40e2
ms.sourcegitcommit: 54baab2a04e5c534fc2d1fd67b67e23a152d4e57
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/04/2020
ms.locfileid: "3019620"
---
# <a name="execution-order-for-initial-synchronization-of-finance-and-operations-apps-and-common-data-service"></a>أمر التنفيذ الخاص بالمزامنة الأولية لتطبيقات Finance and Operations وCommon Data Service

[!include [banner](../../includes/banner.md)]

[!include [preview-banner](../../includes/preview-banner.md)]

قبل استخدام تكامل البيانات، يجب إنشاء البيانات الأولية المطلوبة للعملاء والموردين وجهات الاتصال. على سبيل المثال، تريد إنشاء صنف **مجموعة مورّدين** وتعيين قيمة **شروط الدفع** لها إلى **Net30**. في هذه الحالة، قبل أن تحاول إنشاء صنف **مجموعة المورّدين**، يجب أن تتأكد من وجود **Net30** في كل من التطبيق وCommon Data Service. (في المستقبل، ستقوم Microsoft بإصدار وظيفة نظام أساسي للكتابة المزدوجة تسمى المزامنة الأولية. ستجري هذه الوظيفة مزامنة بيانات لمرة واحدة بين التطبيق وCommon Data Service كجزء من إعداد الكتابة المزدوجة.)

> [!TIP]
> تعمل Microsoft على إصار خريطة كتابة مزدوجة لجميع البيانات المرجعية بما في ذلك **شروط الدفع** (شروط الدفع). إذا كانت البيانات الأولية موجودة في نظام واحد، فبإمكان عملية تحديث صغيرة على سجل أن تؤدي تشغيل الكتابة المزدوجة على هذا السجل.

يجب اتباع ترتيب الأسبقية التالي والتأكد من توفر البيانات الأولية في التطبيق وCommon Data Service.

## <a name="vendor"></a>المورد

فيما يلي ترتيب التنفيذ الخاص بكيان **المورّد**:

1. مجموعة الموردين

    1. شروط الدفع

        1. يوم وبنود الدفع
        2. جدول الدفع

2. طريقة دفع المورّد

## <a name="customer-organization"></a>العميل (مؤسسة)

فيما يلي ترتيب التنفيذ الخاص بكيان **العميل**:

1. مجموعة العملاء

    1. شروط الدفع

        1. يوم وبنود الدفع
        2. المدفوعات 

2. طريقة دفع العميل

## <a name="contact-person"></a>جهة الاتصال (شخص)

فيما يلي ترتيب التنفيذ الخاص بكيان **جهة الاتصال**:

1. العميل
2. المورد
