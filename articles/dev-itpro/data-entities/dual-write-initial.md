---
title: أمر التنفيذ للمزامنة الأولية بين Finance and Operations وCommon Data Service
description: يحدد هذا الموضوع ترتيب المزامنة التي يجب اتباعها لإنشاء البيانات الأولية.
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
ms.openlocfilehash: b74bc2d3133af7e87663a4e6bafb8780e0a6a66f
ms.sourcegitcommit: efcc0dee8bde5f8f93f6291e7f059ad426843e57
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 07/31/2019
ms.locfileid: "1797288"
---
# <a name="execution-order-for-initial-sychronization-of-finance-and-operations-and-common-data-service"></a>أمر التنفيذ للمزامنة الأولية بين Finance and Operations وCommon Data Service

قبل استخدام تكامل البيانات، يجب إنشاء البيانات الأولية المطلوبة للعملاء والموردين وجهات الاتصال. على سبيل المثال، إذا أردت إنشاء صنف **مجموعة موردين** وتعيين **شروط الدفع** على شكل **Net30**، فقبل أن تحاول إنشاء صنف **مجموعة الموردين** يجب أن تتأكد من وجود **Net30** في كل من Finance and Operations وCommon Data Service. (في المستقبل، سنقوم بإصدار وظيفة نظام أساسي للكتابة المزدوجة تسمى **المزامنة الأولية**. ستجري هذه الوظيفة مزامنة بيانات لمرة واحدة بين Finance and Operations وCommon Data Service كجزء من إعداد الكتابة المزدوجة.)

نصائح: نحن بصدد إصار خريطة كتابة مزدوجة لجميع البيانات المرجعية بما في ذلك **شروط الدفع** (شروط الدفع). إذا كانت البيانات الأولية موجودة في نظام واحد، فبإمكان عملية تحديث صغيرة على سجل أن تؤدي تشغيل الكتابة المزدوجة على هذا السجل. 

يجب اتباع ترتيب الأسبقية التالي والتأكد من توفر البيانات الأولية في كل من Finance and Operations وCommon Data Service.   

## <a name="vendor"></a>المورد

ترتيب التنفيذ للمورّد هو:

```
Vendor Group
    Terms of payment
        Payment day & lines
        Payment schedule
Vendor payment method
```

## <a name="customer-organization"></a>العميل (مؤسسة)

ترتيب التنفيذ للعميل هو:

```
Customer Group
    Terms of payment
        Payment day & lines
        Payment 
Customer payment method
```

## <a name="contact-person"></a>جهة الاتصال (شخص)

ترتيب التنفيذ لجهة الاتصال هو:

```
Customer
Vendor               
```
