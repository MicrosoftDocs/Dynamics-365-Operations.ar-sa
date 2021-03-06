---
title: إضافة عنوان لأمر الخدمة
description: يصف هذا الموضوع كيفية إضافة عنوان عميل إلى أمر خدمة.
author: ShylaThompson
manager: tfehr
ms.date: 05/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d6c8f00eb1a1fe2ef3aea22da20ce218d7568f64
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/15/2021
ms.locfileid: "4966045"
---
# <a name="add-an-address-to-a-service-order"></a>إضافة عنوان لأمر الخدمة    

[!include [banner](../includes/banner.md)]


يصف هذا الموضوع كيفية إضافة عنوان عميل إلى أمر خدمة. عند إنشاء أمر خدمة، يتم تحويل معلومات العنوان من المشروع المرفق به أمر الخدمة. ومع ذلك، يمكنك تحديد موقع بديل من العناوين التي تم إدخالها مسبقًا في Microsoft Dynamics AX للعملاء والموردين والمواقع والمستودعات وأوامر الخدمة والمشاريع.

كما يمكن إنشاء عنوان جديد. بشكل افتراضي، يتم تحويل العنوان الجديد للمشروع. ومع ذلك، يمكنك تحديد أن العنوان الجديد مناسبًا فقط لهذا المثيل من الخدمة. إذا قمت بذلك، لا يتم تحويل العنوان الجديد للمشروع.

## <a name="create-a-customer-address-for-a-service-order"></a>إنشاء عنوان العميل لأوامر الخدمة

لإضافة عنوان إلى أمر خدمة، اتبع الخطوات التالية:

1.  انقر فوق **إدارة الخدمة** \> **عام** \> **أوامر الخدمات** \> **أوامر الخدمات**.

2.  افتح أمر الخدمة الذي تريد إنشاء عنوان له.

3.  في **جزء الإجراء**، انقر فوق **تحرير**، ثم انقر فوق **عرض الرأس**.

4.  في علامة التبويب السريعة **عنوان**، انقر فوق **إضافة عنوان**.

5.  في النموذج **عنوان جديد**، أدخل اسمًا فريدًا للعنوان وأكمل الحقول المتبقية. 
    

    > [!WARNING]
    > <P>إذا قمت بإدخال نفس الاسم كعنوان موجود، ستستبدل المعلومات التي يتم إدخالها في الحقول المتبقية معلومات العنوان الموجودة.</P>


6.  انقر فوق **موافق** لنسخ عنوان جديد إلى أمر الخدمة.

## <a name="specify-an-alternative-address-on-a-service-order"></a>تحديد عنوان بديل على أمر خدمة

لإضافة عنوان بديل إلى أمر خدمة، اتبع الخطوات التالية:

1.  انقر فوق **إدارة الخدمة** \> **عام** \> **أوامر الخدمات** \> **أوامر الخدمات**.

2.  افتح أمر الخدمة الذي تريد إدخال عنوان بديل له.

3.  في **جزء الإجراء**، انقر فوق **تحرير**، ثم انقر فوق **عرض الرأس**.

4.  في علامة التبويب السريعة **عنوان**، انقر فوق **عنوان آخر**.

5.  في نموذج **تحديد العنوان** في حقل **نوع سجل**، حدد **أوامر الخدمة**.

6.  حدد عنوانًا ثم انقر فوق **موافق** لنسخه إلى أمر الخدمة.


  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]