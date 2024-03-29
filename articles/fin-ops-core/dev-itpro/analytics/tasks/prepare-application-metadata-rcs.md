---
title: إعداد بيانات تعريف التطبيق لاستخدامها في RCS
description: توضح هذه المقالة كيفية إنشاء تكوين جديد لإعداد التقارير التي تحتوي علي بيانات تعريف التطبيق.
author: kfend
ms.date: 06/28/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2019-06-28
ms.dyn365.ops.version: Version 7.0.0
ms.search.form: ''
ms.openlocfilehash: a9ccbb120be43eaf7a8ae8b5bf8eaafb4850b199
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/12/2022
ms.locfileid: "9289963"
---
# <a name="prepare-application-metadata-to-be-used-in-rcs"></a>إعداد بيانات تعريف التطبيق لاستخدامها في RCS
[!include [banner](../../includes/banner.md)]

توضح الخطوات التالية كيف يمكن لمستخدم يشغل دور المسؤول نظام أو مطور التقارير الإلكترونية إنشاء تكوين التقارير الإلكترونية الجديدة (ER) التي تحتوي علي بيانات تعريف التطبيق لتصميم تكوينات تعيين نموذج ER في Regulatory configuration servic (RCS). يتم استخدام هذا التكوين لتصميم نموذج تكوين تعيين لنموذج ER للوصول إلى حركات التجارية الخارجية. في هذا المثال، ستقوم بإنشاء تكوين لشركة نموذج، .Litware, Inc ويمكن تنفيذ هذه الخطوات في أي شركة. لإكمال هذه الخطوات، يجب أولاً إكمال الخطوات المذكورة في المقالة، [إنشاء موفرات التكوين وتحديدها بالحالة نشط](er-configuration-provider-mark-it-active-2016-11.md).

## <a name="prerequisites"></a>المتطلبات الأساسية
1.    انتقل إلى **إدارة المؤسسة** > **مساحات العمل‬** > **إعداد التقارير الإلكترونية**‬. 
2.    تأكد من وجود موفر التكوين للشركة النموذجية "Litware, Inc." ومن وضع علامة عليه كـ **نشط**. في حالة عدم رؤية موفر التكوين هذا، أكمل الخطوات المذكورة في الإجراء [إنشاء موفرات تكوين وتحديدها بالحالة نشط‬](er-configuration-provider-mark-it-active-2016-11.md). 
3.    انقر فوق **تكوينات بيانات التعريف**. 
4.    افترض أنه سيتم استخدام RCS لتصميم حل ER لتطبيق Finance and Operations والذي سيتم استخدامه لإنشاء مستندات إلكترونية تحتوي على معلومات من مجال أعمال التجارة الخارجية. لتحديد التعيين بين نموذج بيانات ER ومصادر البيانات المطلوبة، يجب أن يكون لديك حق الوصول إلى بيانات تعريف تطبيق Finance and Operations في RCS. وبالتالي، كجزء من عملية تصميم حل ER، نكوِّن بيانات تعريف ER جديدة تحتوي على جميع بيانات التعريف المطلوبة حاليًا من أجل إنشاء تقارير ER لمجال الأعمال المحدد. 

## <a name="add-metadata-configuration"></a>إضافة تكوين ‏‫بيانات التعريف‬ 
1.    انقر فوق **إنشاء تكوين** لفتح مربع حوار الإسقاط‬. 
2.    اكتب في حقل **الاسم** "بيانات تعريف التجارة الخارجية". 
3.    وانقر فوق **إنشاء تكوين**. 
4.    انقر فوق **المصمم**. 
5.    انقر فوق **إضافة**. 
  
> [!NOTE]
> يمكنك تحديد كل بيانات التعريف للتطبيق بالكامل أو النماذج المحددة أو الوحدات النمطية المحددة. يجب مراعاة أنه في هذه الحالة ستتم إضافة بيانات التعريف التالية تلقائيًا: جداول السجلات والتعدادات وأنواع البيانات الملحقة. عند الحاجة لأنواع إضافية من بيانات التعريف، يجب إضافتها يدويًا. 
 
تتوفر لدينا بعض بيانات التعريف المرتبطة بحركات التجارية الخارجية عن طريق تحديد عناصر بيانات التعريف يدويًا. 
  
6.    انقر فوق **إضافة مصدر بيانات**. 
7.    انقر **سجلات الجدول**. 
8.    استخدم عامل التصفية السريع في حقل **الاسم** بالقيمة "نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي". 
9.    حدد سجل جدول **نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي**. 
10.    انقر فوق **موافق**.
  
لقد أضفنا معلومات بيانات التعريف الخاصة بجدول سجلات نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي. 
  
11.    في الشجرة، وسع **علاقات** **نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي بسجلات الجدول**\>. 
12.    في الشجرة، حدد **نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي بسجلات الجدول**\>**Relations\IntrastatCommodity (سجلات جدول EcoResCategory)**.     
13.    انقر فوق **إضافة بيانات تعريف**. 
  
> [!NOTE]
> يجب إضافة بيانات التعريف حول العلاقات المطلوبة لجدول السجلات المحدد يدويًا. 
  
16.    انقر فوق **إضافة مصدر بيانات**. 
17.    انقر فوق **تعداد**. 
18.    استخدم عامل التصفية السريع في حقل **الاسم** بالقيمة "IntrastatDirection". 
19.    حدد سجل **تعداد IntrastatDirection**. 
20.    انقر فوق **موافق**. 
21.    انقر فوق **حفظ**.  
22.    قم بإغلاق الصفحة. 
  
## <a name="complete-the-draft-version-of-metadata-configuration"></a>أكمل الإصدار التمهيدي لتكوين بيانات التعريف
1.    انقر فوق **تغيير الحالة**. 
2.    انقر فوق **إكمال**. 
3.    انقر فوق **موافق**. 
4.    حدد الإصدار المكتمل **1**. 
  
## <a name="export-the-completed-version-of-metadata-configuration-from-application-as-xml-file"></a>صدّر النسخة المكتملة من تكوين بيانات التعريف من التطبيق كملف XML
1.    انقر فوق **تبادل**. 
2.    انقر فوق **تصدير كملف XML**. 
3.    انقر فوق **موافق**. 
    
تم حفظ تكوين بيانات تعريف ER الذي تم إنشاؤه كملف XML يمكن استيراده إلى RCS واستخدامه كمصدر للمعلومات حول بيانات التعريف الخاصة بمجال الأعمال التجارية الخارجية. استنادا إلى هذه المعلومات، يمكننا تحديد التعيين بين بيانات تعريف التطبيق ونموذج بيانات ER.


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
