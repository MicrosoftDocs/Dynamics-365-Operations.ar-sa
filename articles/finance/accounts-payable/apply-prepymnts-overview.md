---
title: تطبيق الدفعات المقدمة لفواتير المورِّدين‬ تلقائيًا
description: يصف هذا الموضوع امكانيه تطبيق الدفعات المقدمة تلقائيا علي فواتير المورد.
author: sunfzam
ms.date: 10/19/2021
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.assetid: ''
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2017-08-30
ms.dyn365.ops.version: 10.0.23
ms.openlocfilehash: 5b07c1d4c2189184b2ad29d46ec2aef0ee03c1c0
ms.sourcegitcommit: 3754d916799595eb611ceabe45a52c6280a98992
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/15/2022
ms.locfileid: "7985352"
---
# <a name="automatically-apply-to-vendor-invoices"></a>تطبيق على فواتير المورِّد بطريقة تلقائية

[!include [banner](../includes/banner.md)]

يصف هذا الموضوع امكانيه تطبيق الدفعات المقدمة تلقائيا علي فواتير المورد. يمكن إنشاء دفعه مقدمه لأمر شراء كجزء من اتفاقيه الشراء. وبعد استلام فاتورة المورد ، يمكن استخدام الدفعة المقدمة لتسويه الحسابات الدائنة من فاتورة المورد. تعمل الميزة الجديدة علي تمكين النظام لاستخدام أرقام أمر الشراء تلقائيا في فاتورة المورد للبحث عن الدفعات المقدمة المقابلة عند استيراد فاتورة المورد.

إذا تم العثور علي دفعات مقدمه ويمكن تطبيقها ، تتم أضافه البنود إلى بنود الفاتورة الموجودة لتطبيق الدفعات المقدمة. لا يتم التعامل مع بنود الدفعة المقدمة أبدا خلال عمليه مطابقه الفاتورة.

تصف النقاط التالية كيفيه تطبيق الدفعات المقدمة عند اتباع عمليات شراء مختلفه:

- **فاتورة مورد واحده لكل أمر شراء** – سيتم تطبيق الدفعة المقدمة في أمر الشراء علي فاتورة المورد.
- **فاتورة مورد واحده لأوامر شراء متعددة** – سيتم تطبيق الدفعات المقدمة في أوامر الشراء علي فاتورة المورد.
- **فواتير مورد متعددة لكل أمر شراء** – سيتم تطبيق الدفعة المقدمة في أمر الشراء علي أول فاتورة مورد مستوردة. إذا قام مبلغ الدفعة المقدمة بتجاوز مبلغ الفاتورة ، سيفشل تطبيق الدفعة المقدمة ، ويجب ان تقوم يدويا بتطبيق الدفعة المقدمة.
- **فواتير مورد متعددة لأوامر شراء متعددة** – سيتم تطبيق الدفعات المقدمة في أوامر الشراء علي أول فاتورة ذات صلة. إذا قام مبلغ الدفعة المقدمة بتجاوز مبلغ الفاتورة ، سيفشل تطبيق الدفعة المقدمة ، ويجب ان تقوم يدويا بتطبيق الدفعات المقدمة. في حاله تطبيق إيه دفعات مقدمه بعد الدفعات المقدمة علي الفاتورة الاولي ، فانه يمكن تطبيقها علي الفواتير التالية.

إذا حاول النظام تطبيق دفعه مقدمه ، ولكن فشل التطبيق ، يعتمد السلوك علي اعداد **معالجه التنفيذ التلقائي لمتابعه الحظر في حاله وجود خيار فشل في تطبيق الدفعة المقدمة**:

- **نعم** – يتم أضافه رسالة الخطا "التطبيق التلقائي للدفعة المقدمة: فشل" في محفوظات التنفيذ التلقائي ، وتبقي الفاتورة في قائمه فواتير المورد المعلقة. ستظل الفاتورة محظوره حتى تقوم بتطبيق الدفعة المقدمة يدويا.

    لتطبيق الدفعات المقدمة يدويا ، انتقل إلى فاتورة المورد المعلقة. في الصفحة **تفاصيل الفاتورة** ، قم بتعيين خيار **تضمين في معالجه مؤتمتة** للفاتورة المحظورة إلى **لا**. يمكنك الآن تطبيق الدفعة المقدمة يدويا. بعد تطبيق الدفعة المقدمة ، قم بتعيين الخيار **تضمين في المعالجة التلقائية** مره أخرى إلى **نعم** حتى يمكن معالجه الفاتورة تلقائيا.

    يمكنك أيضا تجاوز التطبيق التلقائي للدفعة المقدمة عن طريق اعداد خيار **تضمين في معالجه مؤتمتة** إلى **لا** ثم أعاده تعيينه مره أخرى إلى **نعم**. ستتلقى الرسالة التالية: "الدفعة المقدمة موجودة بالفعل لأمر الشراء". هل ترغب في تجاهلها لفاتورة المورد المحددة ؟ " حدد **نعم**. تتم أضافه الرسالة "يتم التجاوز لطلب الدفعة المقدمة يدويا" في محفوظات التنفيذ التلقائي ، ولن يتم حظر فاتورة المورد عند تشغيل العملية التلقائية مره أخرى.

- **لا** – سيتم متابعه عمليات التنفيذ التلقائي للمتابعة. لا يزال بإمكانك تطبيق الدفعة المقدمة اثناء التسوية.