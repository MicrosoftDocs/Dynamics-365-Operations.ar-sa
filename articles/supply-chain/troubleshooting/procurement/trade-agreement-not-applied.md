---
title: شروط الاتفاقية التجارية غير مطبقة على سطور الأوامر المستوردة
description: لا يتم تطبيق أسعار الاتفاقية التجارية والخصومات على بنود أمر الشراء أو المبيعات المستوردة عبر إدارة البيانات
author: kamaybac
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: PurchTable, PurchTablePart, PurchRFQTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: fef38819efaff2f2a927cf09fc7f469490149574
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475500"
---
# <a name="trade-agreement-conditions-arent-applied-to-imported-order-lines"></a>شروط الاتفاقية التجارية غير مطبقة على سطور الأوامر المستوردة

## <a name="symptoms"></a>العلامات

لا يتم تطبيق الاتفاقيات التجارية التي تنطبق على بنود أمر الشراء أو المبيعات على البنود المستوردة عبر إدارة البيانات. ومع ذلك، يتم تطبيق نفس الاتفاقيات التجارية على بنود أمر الشراء أو المبيعات التي يتم إنشاؤها يدويًا.

## <a name="cause"></a>السبب

إذا كانت بنود أمر الشراء المستوردة من خلال إدارة البيانات تتضمن معلومات السعر، فلن يعاد تقييم الاتفاقية التجارية لهذه البنود. على سبيل المثال، إذا تم تعيين **النسبة المئوية لخصم البند‬** أو أي من قيم السعر والخصم لبند ما، فلن يتم البحث عن الاتفاقيات التجارية لذلك البند.

## <a name="workaround"></a>حل بديل

هذا السلوك متوقع، وهو مماثل لأوامر الشراء وأوامر المبيعات على حدٍ سواء.

لحل هذه المشكلة، استورد بنود أمر الشراء بدون تعيين معلومات السعر. سيتم بعد ذلك تطبيق الاتفاقيات التجارية، وسيتم تحديث بنود أمر الشراء استنادًا إلى الاتفاقيات التجارية المحددة.
