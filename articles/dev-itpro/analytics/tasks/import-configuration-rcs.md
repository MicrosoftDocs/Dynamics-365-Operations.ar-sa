---
title: (التقارير الإلكترونية) استيراد التكوينات من RCS
description: يوفر هذا الموضوع معلومات حول كيفية قيام مستخدم باستيراد إصدار جديد من تكوين ER من RCS.
author: NickSelin
manager: AnnBe
ms.date: 07/03/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-07-28
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c458cf815837fb7e4688c4c0443b7962cac403a5
ms.sourcegitcommit: 287d78e6afdaf40c499e5db6c4531f2b26dbaca0
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 07/04/2019
ms.locfileid: "1726996"
---
# <a name="er-import-configurations-from-rcs"></a>(التقارير الإلكترونية) استيراد التكوينات من RCS

[!include [task guide banner](../../includes/task-guide-banner.md)]

تشرح الخطوات التالية كيف يمكن لمستخدم له دور مسؤول النظام أو مطور التقارير الإلكترونية استيراد إصدار جديد من تكوين التقارير الإلكترونية من Microsoft Regulatory Configuration Services (RCS). في هذا المثال، ستقوم بتحديد إصدار تكوين ER الذي تم تكوينه في مثيل RCS واستيراده إلى المثيل الحالي من التمويل الحالي Finance and Operations للشركة النموذجية Litware, Inc. يمكن إجراء هذه الخطوات في أي شركة نظرا لأن تكوينات ER مشتركه بين الشركات. لإكمال هذه الخطوات، في RCS يجب أولاً إكمال الخطوات المذكورة في الموضوع، [إنشاء موفر تكوين ووضع علامة عليه على أنه نشط](er-configuration-provider-mark-it-active-2016-11.md). لإكمال هذه الخطوات، يجب أيضا أن يكون لديك حق الوصول إلى مثيل RCS يحتوي على تكوين ER بالحالة إما **مكتمل** أو **مشترك**.

1. انتقل إلى **إدارة المؤسسة** > **مساحات العمل‬** > **إعداد التقارير الإلكترونية**‬. 
2. تأكد من وجود موفر التكوين للشركة النموذجية "Litware, Inc." ومن وضع علامة عليه كـ **نشط**. إذا لم تشاهد موفر التكوين هذا، فيجب أولاً إكمال الخطوات المذكورة في الموضوع [إنشاء موفر تكوين ووضع علامة عليه على أنه نشط‬](er-configuration-provider-mark-it-active-2016-11.md). 
3. في حالة عدم توفير بيئة RCS للشركة الخاصة بك، انقر فوق الارتباط الخارجي **Regulatory services - التكوين**واتبع الإرشادات لتوفير بيئة RCS. 
4. انقر فوق **معلمات التقارير الإلكترونية**. 
5. انقر فوق علامة التبويب **RCS**. 
6. إذا تم بالفعل توفير بيئة RCS لشركك، فاستخدم المقدم منها على عناوين URL للصفحة للوصول إليها. 
7. قم بإغلاق الصفحة. 

## <a name="register-a-new-er-repository"></a>تسجيل مستودع ER جديد. 
1. في القائمة، قم بوضع علامة للصف المحدد. 
2. حدد الموفر Litware, Inc. 
3. انقر فوق "المستودعات". 
4. انقر فوق "إضافة" لفتح مربع حوار الإسقاط‬. 
5. في الحقل "نوع مستودع التكوين"، أدخل "RCS". 
6. انقر فوق إنشاء مستودع. 
7. في حقل اسم شاشة بيئة RCS، أدخل قيمة أو حددها. 
8. حدد مثيل RCS المرغوب. لاحظ أنه يمكن أن يكون لديك العديد منها. 
9. انقر فوق موافق. 

## <a name="import-er-configurations-from-rcs-based-repository"></a>استيراد تكوينات ER من مستودع تعتمد على RCS
1. انقر فوق **إظهار عوامل التصفية**. 
2. أدخل قيمة عامل التصفية لـ "RCS" في حقل **الاسم** باستخدام مشغل عامل التصفية **يبدأ بـ**. 
3. عند فتح المستودع المحدد، في الصفحة **الاتصال بـ Regulatory Configuration Services**، انقر فوق ارتباط **انقر هنا للاتصال بـ Regulatory Configuration Services**. 
4. انقر فوق **فتح**. 
5. انقر فوق **إغلاق**. 
6. حدد الإصدار المطلوب من تكوين ER ، ثم انقر فوق **استيراد** لإحضاره في مثيل Finance and Operations الحالي.

