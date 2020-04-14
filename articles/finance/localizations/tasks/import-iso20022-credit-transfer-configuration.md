---
title: استيراد تكوين تحويل الائتمان ISO20022
description: يوضح هذا الإجراء كيفية استيراد تكوين التقارير الإلكترونية لمدفوعات المورّد.‬
author: mrolecki
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERVendorPart, ERSolutionRepositoryTable, ERSolutionImport
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 01f44c49b6623cbcc2f08cfd6e4978c9a1676b83
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/18/2020
ms.locfileid: "3140031"
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

