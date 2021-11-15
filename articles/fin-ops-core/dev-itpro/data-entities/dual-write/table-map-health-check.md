---
title: أكواد الأخطاء لفحص صحة تعيين الجدول
description: يوضح هذا الموضوع رموز الأخطاء الخاصة بالتحقق من صحة خريطة الجدول.
author: nhelgren
ms.date: 10/04/2021
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.region: global
ms.author: nhelgren
ms.search.validFrom: 2021-10-04
ms.openlocfilehash: 4f0b92a6bc6c051a6bb24b49d3280ca5ecea3625
ms.sourcegitcommit: c4500b626667185643b3a2e7fc3a004d42198d07
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/29/2021
ms.locfileid: "7725065"
---
# <a name="errors-codes-for-the-table-map-health-check"></a>أكواد الأخطاء لفحص صحة تعيين الجدول

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

يوضح هذا الموضوع رموز الأخطاء الخاصة بالتحقق من صحة خريطة الجدول.

## <a name="error-100"></a>خطأ 100

رسالة الخطا هي "أدنى إصدار مطلوب لنظام Finance and Operations الأساسي هو PU 43 لتشغيل توصيات Finance and Operations."

تتطلب الميزة تحديثات النظام الأساسي للإصدار 10.0.19 أو أحدث لتطبيقات Finance and Operations.

## <a name="error-400"></a>خطأ 400

رسالة الخطا هي "لم يتم العثور علي إيه بيانات تسجيل احداث اعمال للكيان \{Finance and Operations UniqueEntityName\} مما يعني ان الخريطة ليست قيد التشغيل أو ان كافة تعيينات الحقل هي أحادي البعد."

## <a name="error-500"></a>خطأ 500

رسالة الخطا هي "لم يتم العثور علي تكوينات مشروع للمشروع \{اسم المشروع\}. قد يكون هذا اما ان المشروع غير ممكن أو ان كافة تعيينات الحقول هي أحادي البعد من customer engagement ب Finance and Operations . "

تحقق من تعيينات خريطة الجدول. وإذا كانت الاحاديه الحركة من تطبيقات customer engagement للتطبيقات Finance and Operations، فلن يتم إنشاء حركه مرور للمزامنة المباشرة من تطبيقات Finance and Operations إلى Dataverse.

## <a name="error-900"></a>خطأ 900

رسالة الخطا هي "عامل تصفيه مصدر غير صحيح \{sourceFilter\}تنسيق الكيان\{Finance and Operations UniqueEntityName\} "

عامل التصفية المصدر المحدد في خريطة الجدول لتطبيقات Finance and Operations ليست عبارة عن بناء جمله صحيح. للتحقق من صحة معايير التصفية ، راجع [استكشاف مشكلات المزامنة المباشرة وإصلاحها](dual-write-troubleshooting-live-sync.md#live-synchronization-issues-that-are-caused-by-incorrect-query-filter-syntax-on-the-dual-write-maps).

## <a name="error-1000"></a>خطأ 1000

رسالة الخطا هي "الكيان \{Finance and Operations UniqueEntityName\}الاستعلام المستخدم للمزامنة الثنائية للكتابة المباشرة \{Finance and Operations EntityFilterQueryString\}. سيتم انتقاء السجلات التي تطابق معايير الاستعلام للمزامنة المباشرة. "

ويعد الاستعلام عن الكيان الذي تم إرجاعه هو اجراء نسخ احتياطي للاستعلام SQL للكيان. تحقق من وجود صلات أو عوامل تصفيه داخلية علي الاستعلام لتحديد بيانات الاعمال التي يتم انتقاؤها للمزامنة المباشرة. تعتبر الصلات وعوامل التصفية الداخلية حالات إلزاميه يجب تحقيقها لكل سجل يتم انتقاؤه للمزامنة الثنائية للكتابة المباشرة.

## <a name="error-1300"></a>خطأ 1300

رسالة الخطا هي "الحقول الظاهرية \{s.EntityFieldName\} للكيان \{Finance and Operations EntityMetadata.EntityProperties.LogicalEntityName\} قد لا يمكن تعقبها للكتابة المزدوجة."

الحقول الظاهرية من جداول Finance and Operations غير ممكنة للتعقب. يمكن للمزامنة المباشرة مزامنة البيانات ، ولكن لن تتمكن من التقاط التغييرات التي تم اجراؤها علي الاعمده.

## <a name="error-1500"></a>خطأ 1500

رسالة الخطا هي ، "يجب ان يكون هناك حقل واحد علي الأقل معين إلى حقل غير بحث في customer engagement لتمكين التعقب علي مصدر بيانات مصدر البيانات \{datasource.DataSourceName\}."

لا يحتوي مصدر البيانات من الوحدة علي اي حقل تم تعيينه للكتابة المزدوجة. لن يتم تعقب التغييرات التي تم اجراؤها علي الجدول الأساسي للكتابة الثنائية.

## <a name="error-1600"></a>خطأ 1600

رسالة الخطا هي "مصدر البيانات: \{datasource.DataSourceName\} للكيان \{Finance and Operations EntityMetadata.EntityProperties.LogicalEntityName\} يمتلك نطاقًا. يتم انتقاء السجلات التي تفي بشرط النطاق فقط للخارج. "

ويمكن ان يكون للكيانات الموجودة في تطبيقات Finance and Operations مصادر بيانات حيث تكون نطاقات التصفية ممكنة. تحدد هذه النطاقات السجلات التي يتم انتقاؤها كجزء من المزامنة المباشرة. في حاله تخطي بعض السجلات من تطبيقات Finance and Operations إلى Dataverse ، تحقق مما إذا كانت السجلات تفي بمعايير النطاق في الكيان ام لا. ومن الطرق البسيطة للقيام بهذا الفحص تشغيل استعلام SQL الذي يشبه المثال التالي.

```sql
select * from <EntityName> where <filter criteria for the records> on SQL.
```

## <a name="error-1700"></a>خطأ 1700

رسالة الخطا هي "الجدول: \{datasourceTable.Key.subscribedTableName\} للكيان \{datasourceTable.Key.entityName\} يتم تتبع انتيتينامي للكيان \{origTableToEntityMaps.EntityName\}. يمكن ان تؤثر نفس الجداول التي تم تعقبها لكيانات متعددة علي أداء النظام لمعاملات المزامنة المباشرة. "

إذا تم تعقب نفس الجدول بوحدات متعددة ، سيقوم اي تغيير يتم إدخاله علي الجدول بتشغيل تقييم الكتابة الثنائية للكيانات المرتبطة. علي الرغم من ان عبارات عامل التصفية سترسل فقط السجلات الصالحة ، الا ان التقييم قد يتسبب في حدوث مشكله في الأداء إذا كان هناك استعلامات قيد التشغيل أو غير محسن خطط استعلام. قد لا يمكن تجنب هذه المشكلة من منظور الاعمال. ومع ذلك ، ففي حاله وجود العديد من الجداول المتقاطعة عبر كيانات متعددة ، يجب مراعاه تبسيط الكيان أو فحص الامثليه لاستعلامات الكيان.

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
