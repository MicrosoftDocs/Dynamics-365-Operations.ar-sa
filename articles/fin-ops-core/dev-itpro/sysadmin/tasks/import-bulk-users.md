---
title: استيراد المستخدمين من Azure Active Directory
description: يمكن لمسؤولي النظام استخدام هذا الإجراء لاستيراد مستخدمين محددين يدويًا أو استيراد عدد كبير من المستخدمين من Azure Active Directory.
author: peakerbl
ms.date: 07/07/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ce8c98add0c6d5fb07b3ba5338037d9a12b1d8e50a2d2039b0231d3d305c9ebe
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/05/2021
ms.locfileid: "6748278"
---
# <a name="import-users-from-azure-active-directory"></a>استيراد المستخدمين من Azure Active Directory

[!include [banner](../../includes/banner.md)]

## <a name="import-select-users"></a>تحديد استيراد المستخدمين‬

يمكن لمسؤولي النظام استخدام هذا الإجراء لاستيراد مستخدمين محددين من Azure Active Directory (Azure AD).

1. سيتم استيراد المستخدم مع شركة الجلسة الحالية كشركة افتراضية. قم بتغيير الشركة الحالية إن أمكن قبل استيراد المستخدمين.
2. انتقل إلى **إدارة النظام > مستخدمين > مستخدم**.
3. انقر فوق **استيراد المستخدمين**.
4. حدد المستخدمين الذين يجب استيرادهم وحدد **استيراد المستخدمين**.

بعد اكتمال الاستيراد، سيُطلب منك تعيين الأدوار للمستخدمين.

## <a name="import-users-in-bulk"></a>استيراد المستخدمين بشكل مجمع

يمكن استخدام هذا الإجراء من قبل مسؤولي النظام لاستيراد عدد كبير من المستخدمين من خدمة Azure Active Directory.
لاحظ أنه لا يمكن تحديد المستخدمين عند استخدام خيار استيراد الدُفعة.

## <a name="run-the-import-as-a-batch-job"></a>تشغيل الاستيراد كوظيفة دُفعة
1. سيتم استيراد المستخدم مع شركة الجلسة الحالية كشركة افتراضية. قم بتغيير الشركة الحالية إن أمكن قبل استيراد المستخدمين.
2. انتقل إلى **إدارة النظام > مستخدمين > مستخدمين**.
3. انقر فوق **استيراد دُفعة‬**.
4. وسّع القسم **تشغيل في الخلفية‬‬**.
4. حدد **نعم** في حقل **معالجة الدُفعات**.
6. في حقل **مجموعة الدُفعات**، أدخل قيمة أو حددها. هذه خطوة اختيارية.  
7. حدد **نعم** في الحقل **خاص**. هذه خطوة اختيارية.  
8. حدد **نعم** في حقل **وظيفة مهمة**. هذه خطوة اختيارية.  
9. في الحقل **فئة المراقبة**، حدد خيارًا.
10. انقر فوق **موافق**.

بعد اكتمال الاستيراد، سيُطلب منك تعيين الأدوار للمستخدمين.

## <a name="run-in-a-sandbox-environment"></a>التشغيل في بيئة وضع الحماية
1. حدد **استيراد الدُفعات**.
2. حدد **موافق**.


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]