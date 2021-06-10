---
title: تمت مطالبتك بحفظ إعدادات تغطية الصنف حتى إذا لم تقم بأية تغييرات
description: تمت مطالبتك بحفظ إعدادات تغطية الصنف حتى إذا لم تقم بأية تغييرات.
author: ChristianRytt
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: DataManagementWorkspace_
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: angarmas
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 3dfa974740420433af1e1b37630b22509510c91b
ms.sourcegitcommit: 3c15a26e9708adc9a75082dc551f0a3a0a7d89f4
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/17/2021
ms.locfileid: "6049450"
---
# <a name="youre-prompted-to-save-item-coverage-settings-even-though-you-made-no-changes"></a>تمت مطالبتك بحفظ إعدادات تغطية الصنف حتى إذا لم تقم بأية تغييرات

رقم KB: 4615588

## <a name="symptoms"></a>العلامات

في بعض وحدات السيناريو، قد تتلقي الرسالة التالية عند فتح الصفحة **تغطية الصنف** بعد استيراد الأصناف من خلال الكيان *تغطية الصنف V2*:

> هل تريد حفظ التغييرات قبل الإغلاق؟

تظهر لك هذه الرسالة حتى لو لم تقم بإجراء أية تغييرات.

## <a name="resolution"></a>الحل

تتضمن الصفحة **تغطية الصنف** منطق إعداد افتراضي مركب قد يؤدي إلى ظهور الرسالة بعد إجراء التغييرات المباشرة في قاعدة البيانات، مثل استيراد الكيان. على سبيل المثال، يتم تعيين الحقل الكيان `AREGENERALSETTINGSOVERRIDDEN` إلى *No*، لكن إنك تقوم باستيراد ملف يقدم قيم جديدة أو معدلة للحقول مثل `PRODUCTCOVERAGEGROUPID` و/أو `VENDORACCOUNTNUMBER`. في هذه الحالة، بسبب تعيين الحقل `AREGENERALSETTINGSOVERRIDDEN` إلى *لا*، يتم مسح القيم تلقائيًا من الحقول عند فتح الصفحة **تغطية الصنف** لأول مرة بعد عملية الاستيراد. إذا قمت بحفظ التغييرات كلما تطلب مربع الرسالة، فإنه يتم تخزينها في قاعدة البيانات. وإلا، ستتلقى الرسالة نفسها في المرة التالية التي تقوم فيها بفتح الصفحة.

لمنع هذا السلوك ولكن أيضًا لتضمين قيم للحقول مثل `PRODUCTCOVERAGEGROUPID` خلال استيراد الكيان، قم بتعيين `AREGENERALSETTINGSOVERRIDDEN` إلى *نعم* عندما تقوم بالاستيراد.
