---
title: يمكنك إضافة الحساب الرئيسي فقط كحساب دائن لأسباب التسوية
description: عندما تقوم بإعداد سبب تسوية في إدارة النقل، يمكنك إضافة الحساب الرئيسي فقط كحساب دائن.
author: Henrikan
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: TMSFBDetailReconcile
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: c4ba48c5b6e3476c203eed2fddf053ce8af873dd6a7665df54560c8894f8c2d1
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/05/2021
ms.locfileid: "6750872"
---
# <a name="you-can-add-only-the-main-account-as-the-credit-account-for-reconciliation-reasons"></a>يمكنك إضافة الحساب الرئيسي فقط كحساب دائن لأسباب التسوية

رقم KB: 4603538

## <a name="symptoms"></a>العلامات

عندما تقوم بإعداد سبب تسوية في إدارة النقل، يمكنك إضافة الحساب الرئيسي فقط كحساب دائن. لا يمكنك إضافة مركز التكلفة أو أي بعد آخر كحساب دائن. ومع ذلك، يتيح لك حساب المدين تحديد أبعاد أخرى.

## <a name="resolution"></a>الدقة

إذا لم يتم إجراء التسوية لدفع المورد ولكن بالإضافة إلى حساب رئيسي محدد، فلن يسمح النظام بتحديد بُعد مالي لحساب الدائن عند إعداد سبب التسوية.

إذا كانت بنية الحساب تتطلب قيمة بُعد مالي معينة لحساب الدائن الرئيسي، فلا يمكن ترحيل دفتر يومية المورد الناتج تلقائيًا، لأن قيمة البُعد المالي مفقودة. وبالتالي، يجب أولاً تحديد الحساب الدائن يدويًا باستخدام الصفحة **دفتر يومية الفواتير**.

ونظرًا لأن قيمة البُعد مطلوبة للحساب الدائن، فلا يمكن ترحيل دفتر يومية فاتورة المورد تلقائيًا. يجب ترحيلها يدويًا بعد إضافة قيمة البُعد يدويًا إلى الحساب الرئيسي لبند الدائن.
