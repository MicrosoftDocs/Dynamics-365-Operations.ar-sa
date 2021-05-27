---
title: قيمه الحقل غير صحيحة في TaxTrans
description: يوفر هذا الموضوع معلومات حول استكشاف أخطاء قيم الحقول غير الصحيحة وإصلاحها في TaxTrans.
author: bijian
ms.date: 04/27/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: 488ff54f1dd99208db940024a2fe8b2d25861f44
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/11/2021
ms.locfileid: "6020153"
---
# <a name="incorrect-field-value-in-taxtrans"></a>قيمه الحقل غير صحيحة في TaxTrans

[!include [banner](../includes/banner.md)]

إذا كانت قيمة حقل في **TaxTrans** غير صحيحة، استخدم المعلومات الواردة في هذا الموضوع لمحاولة حل المشكلة.

## <a name="overview-of-values"></a>نظرة عامة على القيم
تعرض القائمة التالية مدى تشابه مجموعات بيانات **TaxTrans**، و **TaxUncommitted**، و **TmpTaxWorkTrans**، ولكنها مختلفة في العمل.

  - **TaxTrans** هي النتيجة النهائية لحركة الضريبة المُرحلة التي استمرت في قاعدة البيانات.
  - **TaxUncommitted** هي نتيجة الضريبة الوسيطة المحسوبة الموجودة في قاعدة البيانات (إن وجدت)، والتي سيتم استخدامها لاحقًا في النشر.
  - **TmpTaxWorkTrans** هي نتيجة الضريبة المحسوبة المؤقتة في الجدول الموجود في الذاكرة (نوع الجدول = InMemory).

إذا وجدت السبب الجذري لعمود **TaxTrans**، لقد وجدت أيضًا السبب الجذري لعمود **TaxUncommitted** أو **TmpTaxWorkTrans** غير الصحيح. هذا بسبب نسخ الأعمدة الثلاثة من بعضها البعض.

وعادة ما يتم أثناء حساب الضريبة إنشاء **TmpTaxWorkTrans**، ثم إنشاء **TaxUncommitted** إن أمكن. أثناء ترحيل الضريبة، تم إنشاء **TaxTrans**.


## <a name="add-breakpoints"></a>إضافة نقاط التوقف
لإضافة نقاط توقف، أكمل الخطوات التالية: 

1. أضف الامتدادات ونقاط التوقف في *insert()* و *update()* في الامتدادات كما هو موضح أدناه.

     - **TaxTrans**

        ```x++
        [ExtensionOf(tableStr(TaxTrans))]
        public final class TaxTrans_Extension
        {
            public void insert()
            {
                next insert();
            }
        
            public void update()
            {
                next update();
            }
        
        }
        ```

     - **TaxUncommitted**

        ```x++
        [ExtensionOf(tableStr(TaxUncommitted))]
        public final class TaxUncommitted_Extension
        {
            public void insert()
            {
                next insert();
            }
        
            public void update()
            {
                next update();
            }
        
        }
        ```

     - **TmpTaxWorkTrans**

        ```x++
        [ExtensionOf(tableStr(TmpTaxWorkTrans))]
        public final class TmpTaxWorkTrans_Extension
        {
            public void insert(boolean _ignoreCalculatedSalesTax)
            {
                next insert(_ignoreCalculatedSalesTax);
            }
        
            public void update(boolean _ignoreCalculatedSalesTax)
            {
                next update(_ignoreCalculatedSalesTax);
            }
        
        }
        
        ```

2. بدلاً من ذلك، يمكنك إضافة نقاط توقف مباشرة عند عدم تضمين **TaxUncommitted**.

     - *TaxTrans.insert()*، *TaxTrans.update()*
     - *TmpTaxWorkTrans.insert()*، *TmpTaxWorkTrans.update()*

## <a name="reproduce-and-debug"></a>إعادة الإنتاج والتصحيح

بعد تعيين نقاط التوقف، يكون كل تغيير في استمرارية البيانات مرئيًا أثناء تصحيح الأخطاء. للعثور على السبب الجذري لعمود غير صحيح لـ **TaxTrans** أو **TaxUncommitted** أو **TmpTaxWorkTrans**، راجع ولاحظ العناصر التالية:

- آخر نقطة توقف حيث يكون العمود صحيحًا.
- نقطة الإيقاف الأولى حيث يكون العمود غير صحيح.
- ماذا يحدث بين هاتين النقطتين.

## <a name="determine-whether-customization-exists"></a>حدد ما إذا كان التخصيص موجودًا
إذا كنت قد أكملت الخطوات الواردة في الأقسام السابقة ولكنك لم تتمكن من حل المشكلة، فحدد ما إذا كان التخصيص موجودًا أم لا. إذا لم يكن هناك تخصيص، فاتصل بدعم Microsoft للحصول على المساعدة.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

