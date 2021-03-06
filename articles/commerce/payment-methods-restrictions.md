---
title: تقييد طرق الدفع للمرتجعات من دون إيصال
description: يصف هذا الموضوع كيف يمكن تقييد بعض أنواع الدفع لتلقي المبالغ المستردة إذا تم إجراء عمليات الإرجاع من دون إيصال.
author: rapraj
manager: AnnBe
ms.date: 03/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailTenderTypeTable
audience: Application User
ms.reviewer: josaw
ms.custom: 15831
ms.assetid: 465893a5-6b4f-4c5f-b305-db071df2d33f
ms.search.region: global
ms.search.industry: Retail
ms.author: yabinl
ms.search.validFrom: 2019-02-01
ms.dyn365.ops.version: AX 10.0.0, Retail Feb 2019 update
ms.openlocfilehash: 1ff301aa5f88e34ed7ca24aa54df3fdc7daa1bf7
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/15/2021
ms.locfileid: "5012381"
---
# <a name="restrict-payment-methods-for-returns-without-a-receipt"></a>تقييد طرق الدفع للمرتجعات من دون إيصال


[!include [banner](includes/banner.md)]

يجب أن يتم تكوين كل نوع دفع يقبله بائع التجزئة عند إعداد النظام. يصف هذا الموضوع كيف يمكن تقييد بعض أنواع الدفع لتلقي المبالغ المستردة إذا تم إجراء عمليات الإرجاع من دون إيصال.

## <a name="set-up-payment-methods"></a>إعداد طرق الدفع

لإعداد طرق الدفع، يجب إكمال المهام التالية.
1. أنشئ طرق الدفع التي تم قبولها من قِبل المؤسسة بأكملها.
2. ‏‫أنشئ أنواع البطاقات وأرقام البطاقات على مستوى المؤسسة. وإذا تم قبول بطاقات الدائن أو بطاقات المدين، فيجب إنشاء طريقة دفع واحدة للبطاقات، ثم إنشاء أنواع البطاقات وأرقام البطاقات على مستوى المؤسسة.‬
3. قم بإعداد طرق الدفع في المتجر. اربط طرق الدفع بكل متجر، ثم قم بإدخال الإعدادات الخاصة بالمتجر لكل طريقة دفع.
4. ‏‫قم بإعداد طرق الدفع للمتاجر. وللحصول على أيٍّ من طرق الدفع بالبطاقة التي يقبلها المتجر، استكمل إعداد البطاقة.‬

![إعداد المتجر](media/NoReceiptReturns1.png "إعداد متجر البيع بالتجزئة") 


## <a name="restrict-payment-methods-for-returns-without-a-receipt"></a>تقييد طرق الدفع للمرتجعات من دون إيصال

لكل طريقة دفع في المتجر، في صفحة **إدارة المتاجر**، ضمن **مرتجعات من دون إيصال**، عيّن الخيار **تقييد المبالغ المستردة من دون إيصال** إلى **نعم**. 

القيمة الافتراضية لمفتاح التبديل هي **لا**، مما يضمن السماح لطريقة الدفع باسترداد المبلغ المدفوع. 

عند تعيين الخيار **تقييد المبالغ المستردة من دون إيصال** إلى **نعم**، لن يُسمح لطريقة الدفع باسترداد المبلغ المدفوع. 

![طريقة الدفع بالمتجر](media/NoReceiptReturns3.png "طريقة الدفع في متجر البيع بالتجزئة") 

> [!NOTE]
> عندما يحدد أمين الصندوق طريقة دفع تم فيها تقييد المبالغ المستردة من دون إيصال، تظهر رسالة للتحقق من طرق الدفع المقبولة.

![طرق الدفع المقبولة](media/NoReceiptReturns4.png "طرق الدفع المقبولة") 

إذا تضمنت حركة ما عملية إرجاع مع إيصال وعملية إرجاع من دون إيصال، فلن تُفرض شروط التقييد لأن الحركة ستكون عبارة عن سير عمل إرجاع مع إيصال. 



[!INCLUDE[footer-include](../includes/footer-banner.md)]