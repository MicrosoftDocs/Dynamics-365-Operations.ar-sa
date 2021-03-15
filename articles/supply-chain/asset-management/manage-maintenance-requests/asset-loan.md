---
title: الأصول المقترضة
description: يشرح هذا الموضوع كيفية تسجيل الأصول المقترضة في إدارة الأصول.
author: josaw1
manager: tfehr
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetObjectLoanSend, EntAssetObjectLoanListPage, EntAssetObjectLoanReturn, EntAssetObjectLoanInfoPart
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 355e3d3e0e952db14a03810145528f9701804ca2
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/16/2021
ms.locfileid: "5022322"
---
# <a name="asset-loans"></a>الأصول المقترضة

[!include [banner](../../includes/banner.md)]

 

إذا كانت شركتك تتلقي أصولاً لمهام إصلاح أو صيانة من مواقع داخلية أو عملاء، وإذا قمت مؤخرًا بإقراض الأصول إلى هذه المواقع أو هؤلاء العملاء، فبإمكان إدارة الأصول تعقب الأصول المقترضة.

## <a name="register-asset-loans-on-a-maintenance-request"></a>تسجيل الأصول المقترضة في طلب صيانة

1. حدد **إدارة الأصول** \> **عام** \> **طلبات الصيانة** \> **جميع طلبات الصيانة** أو **طلبات الصيانة النشطة**.
2. حدد طلب الصيانة لتسجيل الأصل المقترض عليه، ثم حدد **تحرير**.
3. في صفحة **الطلب**، حدد **إرسال الأصل المقترض**.
4. حدد الأصل، ثم ادخل تاريخ الإرجاع المتوقع.
5. حدد **موافق**.

> [!NOTE]
> - يمكنك إرسال أصل مقترض فقط إذا توفر لديك أصل من نوع الأصل نفسه.
> - يجب أن يكون للأصل المقترض حالة دورة حياة أصل تسمح باستخدامه كـصل مقترض، مثل **InStorage**. عند تسجيل الأصل المقترض، يتم تلقائيًا تحديث حالة دورة حياة الأصل الخاصة بالأصل بشكل تلقائي إلى، على سبيل المثال، **OnLoan**.

لعرض قائمة بكافة الأصول التي قمت بإقراضها إلى مواقع أو عملاء آخرين، حدد **إدارة الأصول** \> **عام** \> **أصل مقترض** \> **جميع الأصول المقترضة**. إذا كانت خانة الاختيار **منتهٍ** لأحد الأصول محددة، فهذا يعني أنه تم تسجيل الأصل كما تم إرجاعه إلى شركتك.

![إدارة طلبات الصيانة](media/06-manage-maintenance-requests.png)

في صفحة **الأصول المقترضة النشطة**، يمكنك عرض قائمة بجميع الأصول المقترضة التي لم يتم إرجاعها بعد إلى شركتك.

## <a name="register-loan-assets-as-returned"></a>تسجيل الأصول المقترضة كمرتجعة

1. حدد **إدارة الأصول** \> **عام** \> **أصل مقترض** \> **الأصول‏‎ المقترضة النشطة**.
2. حدد الأصل المقترض لتسجيله كمرتجع، ثم حدد **إرجاع الأصل المقترض**.
3. في الحقل **مُرتجع‬**، أدخل التاريخ والوقت.
4. حدد **موافق**.
5. قم بتحديث صفحة **الأصول المقترضة النشطة**، ولاحظ عدم ظهور الأصل المقترض في القائمة.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]