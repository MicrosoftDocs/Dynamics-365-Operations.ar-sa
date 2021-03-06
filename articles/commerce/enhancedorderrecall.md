---
title: إعادة استدعاء عملية الأمر في نقطة البيع
description: يشرح هذا الموضوع إمكانيات الميزات المتوفرة لطلب تحسين صفحات الاستدعاء في POS.
author: hhainesms
manager: annbe
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: global
ms.author: hhaines
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 21e8045d754006345f5ad68e1e67579386c6df4a
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/15/2021
ms.locfileid: "5010064"
---
# <a name="recall-order-operation-in-pos"></a>إعادة استدعاء عملية الأمر في نقطة البيع

[!include [banner](includes/banner.md)]

توفر ‏ عملية **إعادة استدعاء الأمر** في نقطة بيع (POS) Commerce ميزات بحث وتصفية مُحدّثة ومعلومات خاصة بالأمر. تتوفر هذه الميزة في الإصدار 10.0.15 من Commerce والإصدارات اللاحقة.

لتمكين هذه الوظيفة، قم بتشغيل ميزة **عمليه أمر أعاده الاستدعاء المحسنة في POS** في مساحة عمل **أداره الميزات** في مركز Commerce الرئيسي. بعد تمكين الميزة ، حاول تحديث [تخطيطات الشاشة](pos-screen-layouts.md)في نقطه البيع للاستفادة من الإمكانيات التي تم تغييرها.

يسمح تكوين زر عملية **أمر الاستدعاء** للمؤسسات لنشر العملية بعرض معرف مسبقا.

![تكوين شبكة الزر](media/recallorderbuttongrid.png)

وخيارات العرض كما يلي.
- **بلا** – يقوم هذا الخيار بنشر العملية بدون عرض محدد. عندما يقوم أحد المستخدمين بفتح العملية باستخدام هذا التكوين، ستتم مطالبتهم بالبحث عن الأوامر والبحث عنها أو الاختيار من عامل تصفيه أمر معرف مسبقا.
- **الأوامر المطلوب تنفيذها** -عندما يقوم مستخدم ببدء العملية، سيتم تشغيل استعلام تلقائيا للبحث عن قائمه بالأوامر التي سيتم استيفاؤها في المتجر وعرضها. يتم تكوين هذه الأوامر للالتقاط في المتجر أو الشحنة المتجر ولم يتم بعد انتقاء بنود هذه الأوامر أو تعبئتها.
- **الأوامر المطلوب تنفيذها** -عندما يقوم مستخدم ببدء العملية، سيتم تشغيل استعلام تلقائيا للبحث عن قائمه بالأوامر التي سيتم تكوينها للاستلام داخل المتجر وعرضها للمتجر الحالي للمستخدم.
- **الأوامر المطلوب شحنها** - عندما يقوم مستخدم ببدء العملية، سيتم تشغيل استعلام تلقائيا للبحث عن قائمه بالأوامر التي سيتم تكوينها للشحن من المتجر الحالي للمستخدم.

عند تشغيل عمليه **أمر الاستدعاء** من نقطه البيع، إذا تم تكوين العرض علي **بلا**، سيكون بإمكان المستخدم البحث عن الأوامر واستردادها بأحدي الطرق التالية.
- امسح الرموز الشريطية للأمر. سيؤدي ذلك إلى البحث في رقم الأمر ومرجع القناة وحقول معرف الاستلام للتطابقات المطابقة.
- حدد أيقونة **أوامر البحث** أو **البحث والتصفية** في شريط التطبيقات لاستخدام اليه التصفية لتحديد موقع الطلبات التي تفي بمعايير التصفية.
- يمكنك الاختيار من عامل تصفيه معرف مسبقا من القائمة المنسدلة **إظهار الأوامر** (طلبات مطلوب تنفيذها أو طلبات مطلوب استلامها أو طلبات مطلوب شحنها).

![القائمة الرئيسية لأوامر الاستدعاء](media/recallordermain.png)

بعد تطبيق معايير البحث، سيعرض التطبيق قائمه بأوامر المبيعات المطابقة.

![تفاصيل أمر الاستدعاء](media/orderrecalldetail.png)

يمكن للمستخدم تحديد أحد الأوامر في القائمة لعرض تفاصيل اضافيه. تعرض لوحه المعلومات الموجودة علي الجانب الأيسر التفاصيل حول الأمر المحدد، بما في ذلك تفاصيل بند الأمر وتفاصيل التسليم وتفاصيل الإنجاز.

من شريط التطبيقات، يمكن للمستخدم تحديد عمليه. ووفقا لحاله الأمر، قد لا يتم تمكين بعض العمليات.

- **إرجاع** – يستخدم في تنفيذ إرجاع لفاتورة واحده أو أكثر مرتبطة بامر العميل المحدد.

- **إلغاء الأمر** – إصدار عمليه إلغاء كامله لأمر التوريد المحدد.

- **التنفيذ** – تحويل المستخدم إلى صفحه استيفاء الأوامر، والذي سيتم تصفيته مسبقا للأمر المحدد. سيتم فقط عرض سطور الأمر المفتوحة لاستيفائها بواسطة متجر المستخدم للأمر المحدد.

- **تحرير** – يتيح للمستخدمين اجراء تغييرات علي أمر العميل المحدد.

- **استلام** – بدء تشغيل تدفق الاستلام، والذي يسمح للمستخدم باختيار المنتجات التي سيتم استلامها وإنشاء حركه مبيعات للاستلام.


[!INCLUDE[footer-include](../includes/footer-banner.md)]