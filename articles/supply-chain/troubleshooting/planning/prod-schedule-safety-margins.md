---
title: لا تراعي جدولة الإنتاج حدود الأمان
description: لا تعد جدوله الإنتاج بعين الاعتبار حدود الأمان التي تم تعيينها في تغطيه الصنف لتوريد مثبت
author: ChristianRytt
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 738296b7570ded0a4ee806e4445204a68e6a08c8
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475451"
---
# <a name="production-scheduling-doesnt-consider-the-safety-margins"></a>لا تراعي جدولة الإنتاج حدود الأمان

## <a name="symptoms"></a>العلامات

يعتبر التخطيط الرئيسي بالمثل حدود الأمان. ومع ذلك ، يتم تجاهل حدود الأمان عندما تتم جدوله أوامر الإنتاج المخططة.

## <a name="resolution"></a>الحل

يتم التعامل مع الهوامش فقط اثناء التخطيط الرئيسي ، وليس اثناء الجدولة اليدوية. يتم تصميم الهوامش لتعمل كمخزن مؤقت اثناء مرحله التخطيط ، وذلك لإعطاء بعض "الهوامش" للعملية الفعلية.

للحصول علي النتيجة المطلوبة ، يمكنك أزاله الهامش. ويجب بعد ذلك تحديث المسار حتى يتضمن الوقت المرغوب فيه (علي سبيل المثال ، وقت قائمه الانتظار). يجب ان ينتج عن كل من التخطيط الرئيسي والجدولة اليدوية بعد ذلك النتيجة.
