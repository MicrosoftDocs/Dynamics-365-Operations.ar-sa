---
title: الفجوات الوظيفية بين تقارير قيمة/تقادم المخزون وإصدارات التخزين الخاصة به
description: الفجوات الوظيفية بين تقارير قيمة/تقادم المخزون وإصدارات التخزين الخاصة به
author: AndersGirke
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: InventAgingStorage, InventAgingStorageChart, InventAgingStorageDetails
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: f74389648034bf036ce48ac84b3421a8a340f105
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/04/2022
ms.locfileid: "8686642"
---
# <a name="functional-gaps-between-inventory-valueaging-reports-and-their-storage-versions"></a>الفجوات الوظيفية بين تقارير قيمة/تقادم المخزون وإصدارات التخزين الخاصة به

تتيح ميزتا [تقرير فتره تاخر المخزون](/dynamics365/supply-chain/cost-management/inventory-aging-report-storage) و[تخزين قيمه المخزون الخاصة بها](/dynamics365/supply-chain/cost-management/inventory-value-report-storage)امكانيه Supply Chain Management لعرض وحدات التخزين الكبيرة الخاصة بالعمليات المخزنية. في كل حاله ، يتم حفظ نتائج التقرير للاستعراض والتصدير ، بخلاف الإصدارات غير الخاصة بالتخزين لهذه التقارير. ومع ذلك ، لا توجد بعض الوظائف الموجودة في الإصدارات غير الخاصة بالتخزين من هذه التقارير في إصدارات التخزين. تلخص الأقسام الفرعية التالية الاختلافات وتوفر حلول بديله.

## <a name="storage-reports-dont-include-subtotals-even-if-they-are-enabled-in-the-report-layout"></a>لا تتضمن تقارير التخزين الإجماليات الفرعية ، حتى ولو كانت ممكنة في تخطيط التقرير

ويمكن ان يتسبب الإجماليات الفرعية في حدوث مشكلات عند تصدير النتيجة ، وخاصه إذا قام المستخدمون بتغيير تسلسل السجلات.

لفحص الإجماليات الفرعية ، يمكنك تصدير النتيجة إلى Microsoft Excel. بدلا من ذلك، إذا كنت ترغب في التحقق من الإجماليات الفرعية ضمن Supply Chain Management، استخدم [أداره الميزات](/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview) لتمكين ميزتي *التحكم بالشبكة الجديد* و *تجميع في الشبكة*، والتي توفر طريقه أكثر مرونة لمشاهده الإجمالي الفرعي لأي مجموعه حسب العمود. لمزيد من المعلومات، راجع [قدرات الشبكة](/dynamics365/fin-ops-core/fin-ops/get-started/grid-capabilities).

## <a name="inventory-value-storage-report-doesnt-support-ledger-account-information"></a>تقرير تخزين قيمه المخزون لا يدعم معلومات حساب دفتر الأستاذ

يمكنك تشغيل الرصيد التجريبي للحصول علي رصيد حسابات المخزون ومقارنته بتقرير **تخزين قيمه المخزون**.
