---
title: يجب أن تكون قيمة الوزن موجبة
description: يجب أن تكون قيمة الوزن موجبة
author: perlynne
ms.date: 04/15/2021
ms.topic: troubleshooting
ms.search.form: WHSContainerCloseDiag_canClose
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-05-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: dcbcde3143cb509b68b277cb7c709263e2659b5b
ms.sourcegitcommit: 5f5afb46431e1abd8fb6e92e0189914b598dc7fd
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/21/2021
ms.locfileid: "5924293"
---
# <a name="weight-must-be-positive"></a>يجب أن تكون قيمة الوزن موجبة

رمز الخطأ: WeightMustBePositive

## <a name="symptoms"></a>العلامات

يعرض النظام رسالة الخطأ التالية:

> يجب أن تكون قيمة الوزن موجبة.

## <a name="cause"></a>السبب

تم تعيين حقل **الوزن الإجمالي** إلى *0* (صفر) أو قيمة سالبة.

## <a name="resolution"></a>الدقة

لتحديد الوزن، اتبع إحدى هذه الخطوات.

- في حقل **الوزن الإجمالي**، قم بتعيين قيمة. وحدد بعد ذلك وحدة في القائمة المنسدلة.
- حدد **الحصول على وزن النظام** لحساب قيمة **الوزن الإجمالي**.
