---
title: يعمل التخطيط الرئيسي على إنشاء أوامر مخططة للمنتجات الوهمية
description: يتم إنشاء الأوامر المخططة للمنتجات الوهمية بعد تشغيل التخطيط الرئيسي.
author: ChristianRytt
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPo
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: anderso
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: f3170bcb723e2d7483258bb0ecf786e62f2aa3d196745074c2ac554bc212ec55
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/05/2021
ms.locfileid: "6741994"
---
# <a name="master-planning-generates-planned-orders-for-phantom-products"></a>يعمل التخطيط الرئيسي على إنشاء أوامر مخططة للمنتجات الوهمية

رقم KB: 4614729

## <a name="symptoms"></a>العلامات

يتم إنشاء الأوامر المخططة للمنتجات الوهمية بعد تشغيل التخطيط الرئيسي.

## <a name="resolution"></a>الدقة

يحدد إعداد الخيار **صنف وهمي** الخاص بالمنتجات التي تم إصدارها نوع البند الافتراضي في شجرة المواد (BOM). عند تعيين الخيار **صنف وهمي** على *نعم*، سيستمر النظام في إنشاء أوامر مخططة للصنف، ولكن يتم تعيين الخيار **متطلب مشتق مباشرة** لكل أمر مخطط على *نعم*. وبالتالي، لا يمكن تأكيد أمر الإنتاج المخطط بنفسه. وبدلاً من ذلك، سيتم تضمينها تلقائيًا عند تأكيد أمر الإنتاج الأصلي. بالإضافة إلى ذلك، سيتم تضمين بنود قائمة مكونات الصنف (BOM) للصنف الوهمي المخطط في قائمة مكونات الصنف (BOM) لأمر الإنتاج الأصلي.
