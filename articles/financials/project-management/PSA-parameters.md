---
title: محددات تكامل Project Service Automation
description: يشرح هذا الموضوع كيفية تكوين طريقة إدخال البيانات الافتراضية عند تمكين تكامل Microsoft Dynamics 365 for Project Service Automation مع Microsoft Dynamics 365 for Finance and Operations.
author: KimANelson
manager: AnnBe
ms.date: 07/20/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: 33960a97f69d6bcc70a3035d4d68095ca6993a10
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/15/2019
ms.locfileid: "1557273"
---
# <a name="project-service-automation-integration-parameters"></a>معلمات تكامل Project Service Automation

[!include[banner](../includes/banner.md)]

في صفحة **معلمات تكامل Project Service Automation‬**، يمكنك تكوين كيفية إدخال البيانات الافتراضية عند تمكين تكامل Microsoft Dynamics 365 for Project Service Automation مع Microsoft Dynamics 365 for Finance and Operations. لكي تتم مزامنة المشاريع بشكل ناجح من Project Service Automation إلى Finance and Operations، يجب إعداد الحقول التالية.

> [!NOTE]
> - تتوافر ميزات تكامل مهام المشروع وفئات حركات المصروفات وتقديرات عدد الساعات وتقديرات المصروفات وتأمين الوظيفة في الإصدار 8.0 من Microsoft Dynamics 365 for Finance and Operations.
> - يتوفر تكامل القيم الفعلية في الإصدار 8.0.1 أو إصدار لاحق من Microsoft Dynamics 365 for Finance and Operations.
> - إذا كنت تستخدم Microsoft Dynamics 365 for Finance and Operations, Enterprise edition 7.3.0، بعد قيامك بتثبيت قاعدة المعارف 4132657 وقاعدة المعارف 4132660، ستكون قادرًا على استخدام القوالب لتمكين تكامل مهام المشاريع وفئات حركات المصروفات وتقديرات عدد الساعات وتقديرات المصروفات والقيم الفعلية وتكوين تأمين الوظيفة. إذا كان يجب عليك إعادة تعيين التوزيعات المحاسبية، فمن المستحسن أن تقوم أيضًا بتثبيت قاعدة المعارف 4131710.

| علامة تبويب                    | الحقل                | الوصف |
|------------------------|----------------------|-------------|
| عام                | نوع المشروع الافتراضي | حدد نوع المشروع الافتراضي. عند مزامنة المشاريع من Project Service Automation، تُستخدم هذه القيمة إذا لم تحدد قيمة افتراضية في قالب التكامل. أثناء المزامنة، يتم تعيين حقل **نوع المشروع** للمشاريع الجديدة إلى هذه القيمة. ومع ذلك، قد يتم تحديث القيمة عندما تتم مزامنة بنود عقد المشروع من Project Service Automation. |
|                        | فئة الوقت        | حدد فئة الوقت الافتراضية. يتم استخدام هذه القيمة عند مزامنة تقديرات الساعات من Project Service Automation. عند مزامنة تقديرات الساعات والقيم الفعلية للساعات من Project Service Automation، يتم تعيين حقل **الفئة** لتقديرات ساعات المشروع الجديد في Finance and Operations إلى هذه القيمة. |
|                        | فئة الرسوم         | حدد فئة الرسوم الافتراضية. يتم استخدام هذه القيمة عند مزامنة القيم الفعلية للرسوم من Project Service Automation. عند مزامنة القيم الفعلية للرسوم من Project Service Automation، يتم تعيين حقل **الفئة** لحركات الرسوم الجديدة في Finance and Operations إلى هذه القيمة. |
| القيم الافتراضية لمجموعة المشاريع | نوع المشروع         | انقر فوق **جديد** لإضافة صف حيث يمكنك تحديد نوع المشروع لتعيين مجموعة المشاريع الافتراضية له. يمكن تحديد نوع مشروع محدد مرة واحدة فقط في التكوين. |
|                        | تصنيف المشروع        | حدد مجموعة المشاريع الافتراضية لنوع المشروع المحدد. عند مزامنة مشروعات جديدة من Project Service Automation، يتم تعيين حقل **مجموعة المشاريع** إلى القيمة الافتراضية لنوع المشروع إذا لم تحدد قيمة افتراضية في قالب التكامل. |
| القيم الافتراضية لنوع الفوترة  | نوع الفوترة         | انقر فوق **جديد** لإضافة صف حيث يمكنك تحديد نوع الفوترة لتعيين خاصية البند الافتراضي له. يمكن تحديد نوع فوترة محدد مرة واحدة فقط في التكوين. |
|                        | خاصية السطر        | حدد خاصية البند الافتراضي لنوع الفوترة المحدد. عند مزامنة تقديرات عدد الساعات الجديدة أو تقديرات المصروفات الجديدة أو القيم الفعلية الجديدة من Project Service Automation، يتم تعيين حقل **خاصية البند** إلى القيمة الافتراضية لنوع الفوترة. |
| تأمين الوظيفة  | غير قابل للتطبيق       | حدد الوظيفة التي يتم عندها التعطيل في Finance and Operations بالنسبة للمشاريع والعقود التي تم إنشاؤها من Project Service Automation. على سبيل المثال، يمكنك إيقاف تشغيل القدرة على تحرير العقود والمشاريع، وإنشاء هياكل تنظيم العمل وإدخال جداول زمنية في Finance and Operations. سوف يستمر تمكين الحقول المرتبطة بالمحاسبة، حتى لو ألغيت إتاحتها من خلال إعداد المُعلمة. بشكل افتراضي، تكون كافة الوظائف ممكّنة. |
