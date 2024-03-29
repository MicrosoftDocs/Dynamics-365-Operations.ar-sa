---
title: استيراد تكوين تحويل الائتمان ISO20022
description: يوضح هذا الإجراء كيفية استيراد تكوين التقارير الإلكترونية لمدفوعات المورّد.‬
author: mrolecki
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERVendorPart, ERSolutionRepositoryTable, ERSolutionImport
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ffc86ba9dade0ae494ca4ace8d9f562da9c9527a4731493d892b60112293af3f
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/05/2021
ms.locfileid: "6781126"
---
# <a name="import-iso20022-credit-transfer-configuration"></a>استيراد تكوين تحويل الائتمان ISO20022

[!include [banner](../../includes/banner.md)]

يوضح هذا الإجراء كيفية استيراد تكوين التقارير الإلكترونية لمدفوعات المورّد.‬ يتم استخدام تنسيق تحويل الائتمان الألماني ISO 20022 كمثال. يمكنك استخدام هذا الإجراء لتنسيقات التقارير الإلكترونية الأخرى المتوفرة. 

تم إنشاء هذه المهمة باستخدام شركة بيانات العرض التوضيحي DEMF، ولكن يمكنك استخدام أي من شركات بيانات العرض التوضيحي لإكمال هذه المهمة.

هذه هي المهمة الأولى من ضمن خمس مهام، هدفها أن تعمل معًا على توضيح عملية معالجة مدفوعات المورّد باستخدام تكوينات التقارير الإلكترونية. يتم استخدام هذا الإجراء لميزة تمت إضافتها في Dynamics 365 for Operations، الإصدار 1611.

1. انتقل إلى إدارة المؤسسة > مساحات العمل‬ > إعداد التقارير الإلكتروني‬.
2. في قائمة "موفرو التكوين‬" المتوفرون، حدد Microsoft.
3. انقر فوق "تعيين كنشط".
4. انقر فوق "المستودعات".
5. انقر فوق "فتح".
6. انقر فوق "إظهار عوامل التصفية".
7. طبّق عوامل التصفية التالية: أدخل قيمة عامل التصفية "تحويل الائتمان ISO20022 (DE)" في حقل "اسم التكوين" باستخدام مشغل عامل التصفية "يبدأ بـ".
    * أو، يمكنك العثور على التكوين في القائمة، وتحديده، ثم نقله إلى مهمة الاستيراد.  
8. انقر فوق "استيراد".
    * إذا لم يتوفر الزر "استيراد"، فهذا يعني أن التكوين قد تم استيراده.  
9. انقر فوق نعم.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]