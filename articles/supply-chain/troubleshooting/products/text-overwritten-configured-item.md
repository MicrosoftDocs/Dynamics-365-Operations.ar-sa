---
title: تتم الكتابة فوق النص عند تكوين صنف في بند أمر المبيعات
description: عند تكوين منتج في بند أمر المبيعات، تتم الكتابة فوق النص المعدل بنص قياسي. يجب تغيير النص بعد تكوين البند، وليس قبل ذلك.
author: SmithaNataraj
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 20239b9b0eecb355274e909a8b8b39450e468c7e
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475426"
---
# <a name="item-text-is-overwritten-when-a-product-is-configured-on-a-sales-order-line"></a>تتم الكتابة فوق نص الصنف عند تكوين منتج في بند أمر التوريد

## <a name="symptoms"></a>العلامات

تحدث هذه المشكلة عند إنشاء بند أمر المبيعات لصنف قابل للتكوين ثم تعديل نص الصنف. عند تكوين الصنف وتحديد **موافق**، تتم الكتابة فوق النص بالنص القياسي.

## <a name="resolution"></a>الحل

هذا السلوك متوقع. يتضمن حقل النص اسم المتغير ، والذي يتم ملؤه فقط بعد تكوين البند. التالي ، يجب تغيير النص بعد تكوين البند ، وليس قبل ذلك.
