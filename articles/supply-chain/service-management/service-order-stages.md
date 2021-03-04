---
title: مراحل أمر خدمة
description: من خلا تحديد مراحل لأمر الخدمة وتعيينها إلى العاملين، فإنك تتحكم في تدفق أمر الخدمة من خلال المهام التي ينفذها العديد من الأشخاص في مؤسسة الخدمة.
author: ShylaThompson
manager: tfehr
ms.date: 04/30/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceOrderTable, SMAStageTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 52bcb72e8222b378198fcd044428fa1a4a0e8944
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/13/2020
ms.locfileid: "4421052"
---
# <a name="service-order-stages"></a>مراحل أمر خدمة   

[!include [banner](../includes/banner.md)]


يمكنك إعداد مراحل أمر الخدمة لتحديد المهام التي يجب إكمالها والترتيب الذي يتم إكمالها به والعاملين المسؤولين عن الانتهاء منها. بتحديد مراحل لأمر الخدمة وتعيينها إلى العاملين، يمكن التحكم في تدفق أمر الخدمة من خلال المهام التي ينفذها العديد من الأشخاص في مؤسسة الخدمة. يجب أن يحتوي تسلسل المراحل على مرحلة أولية.

يمكنك أيضا تعريف الإجراءات المسموح بها في كل مرحلة. على سبيل المثال، إذا قمت بإلغاء تحديد خانة الاختيار **ترحيل** لجميع المراحل باستثناء المرحلة النهائية، فإنه يتم بذلك منع ترحيل أية أوامر خدمة قبل أن تتم معالجة أوامر الخدمة عبر تسلسل المراحل بأكمله.

## <a name="branching-in-service-order-stages"></a>التفريع في مراحل أمر الخدمة

عند إعداد مرحلة خدمة، يمكنك إنشاء خيارات متعددة أو فروع، للتحديد من بينها لمرحلة الخدمة التالية. تتوفر كافة الفروع التي تقوم بإنشائها للاختيار من بينها عند اكتمال المرحلة الأولية. على سبيل المثال، يمكنك إعداد **التخطيط** كمرحلة أولية. يمكنك إنشاء مرحلتين تحملان الإسمين **قيد التنفيذ** و **إلغاء**، ثم تحديد **التخطيط** لتكون المرحلة الأصل الخاصة بهما. قم بتعيين مرحلة **التخطيط** إلى أمر المبيعات. عند اكتمال مرحلة التخطيط لأمر المبيعات، يمكنك تحديد مرحلة **قيد التنفيذ** إذا كان أمر المبيعات جاهز للعمل، أو يمكنك تحديد مرحلة **إلغاء** إذا تم إلغاء أمر المبيعات.

## <a name="see-also"></a>راجع أيضًا

[إعداد مراحل أمر الخدمة](set-up-service-order-stages.md)

[تغيير مرحلة أمر الخدمة](change-service-order-stage.md)

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]