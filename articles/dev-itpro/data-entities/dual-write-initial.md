---
title: أمر التنفيذ للمزامنة الأولية بين Finance and Operations وCommon Data Service
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
ms.openlocfilehash: 1473c3bad55734d5f83ee3e4c1654921b872f3bb
ms.sourcegitcommit: 3f05ede8b8acdf0550240a83a013e093b4ad043d
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/13/2019
ms.locfileid: "1873118"
---
# <a name="execution-order-for-initial-synchronization-of-finance-and-operations-and-common-data-service"></a>أمر التنفيذ للمزامنة الأولية بين Finance and Operations وCommon Data Service

[!include [banner](../includes/banner.md)]

[!include [preview](../includes/preview-banner.md)]

قبل استخدام تكامل البيانات، يجب إنشاء البيانات الأولية المطلوبة للعملاء والموردين وجهات الاتصال. على سبيل المثال، تريد إنشاء صنف **مجموعة مورّدين** وتعيين قيمة **شروط الدفع** لها إلى **Net30**. في هذه الحالة، قبل أن تحاول إنشاء صنف **مجموعة المورّدين**، يجب أن تتأكد من وجود **Net30** في كل من Microsoft Dynamics 365 for Finance and Operations وCommon Data Service. (في المستقبل، ستقوم Microsoft بإصدار وظيفة نظام أساسي للكتابة المزدوجة تسمى المزامنة الأولية. ستجري هذه الوظيفة مزامنة بيانات لمرة واحدة بين Finance and Operations وCommon Data Service كجزء من إعداد الكتابة المزدوجة.)

> [!TIP]
> تعمل Microsoft على إصار خريطة كتابة مزدوجة لجميع البيانات المرجعية بما في ذلك **شروط الدفع** (شروط الدفع). إذا كانت البيانات الأولية موجودة في نظام واحد، فبإمكان عملية تحديث صغيرة على سجل أن تؤدي تشغيل الكتابة المزدوجة على هذا السجل.

يجب اتباع ترتيب الأسبقية التالي والتأكد من توفر البيانات الأولية في كل من Finance and Operations وCommon Data Service.

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
