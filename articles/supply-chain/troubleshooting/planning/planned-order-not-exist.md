---
title: يتعذر علي النظام العثور علي أمر مخطط اثناء العمليات في أوامر متعددة
description: يحدث الخطا "الأمر المخطط غير موجود" عند اجراء عمليات في العديد من الأوامر المخططة، وينتمي أمرين علي الأقل إلى نفس معرف الصنف.
author: t-benebo
ms.date: 12/07/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPo_ReqTransPoMarkChangeType
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2021-12-07
ms.dyn365.ops.version: 10.0.24
ms.openlocfilehash: 0ece4a331b63b86e896c5b337a58185ed3ea1049
ms.sourcegitcommit: 008779c530798f563fe216810d34b2d56f2c8d3c
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 12/14/2021
ms.locfileid: "7920787"
---
# <a name="the-system-cant-find-a-planned-order-during-operations-on-multiple-orders"></a>يتعذر علي النظام العثور علي أمر مخطط اثناء العمليات في أوامر متعددة

رمز الخطأ: SYS24774

## <a name="symptoms"></a>العلامات

وتظهر رسالة الخطا التالية عند محاولة تنفيذ عمليه في العديد من الأوامر المخططة في نفس الوقت، وينتمي الأمران علي الأقل إلى نفس معرف الصنف. علي سبيل المثال، قد يحدث الخطا عند تاكيد الأوامر أو إذا تم تغيير نوع الطلب الخاص بها.

> أمر التوريد المخطط %1 غير موجود.

## <a name="cause"></a>السبب

عندما يقوم النظام بتأسيس نوع الأمر أو تغييره، يجب أن يعيد النظر في الأوامر المخططة الحالية للصنف، للتأكد من أن التوريد المخطط له يتطابق مع الطلب والعرض الحالي. كجزء من هذه العملية، يقوم النظام باعاده إنشاء أوامر مخططه للصنف. لذلك، لا تعود الأوامر المخططة الثانية التي يتوقعها النظام لمعالجتها موجودة.

## <a name="workaround"></a>حل بديل

اعتماد الأوامر قبل معالجتها. وبهذه الطريقة، لن يتم حذف الأوامر عندما يقوم النظام بمعالجه الترتيب الأول للصنف.
