---
title: لا يعمل جزء التصفية على صفحة القائمة الفعلية كما هو متوقع
description: لا تقوم عوامل التصفية في جزء التصفية الموجود في الصفحة "القائمة الفعلية" بتصفية النتائج كما تتوقعها.
author: sherry-zheng
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: df11b1c1e7de36fa0458cd931d4be7f84a15d143
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475501"
---
# <a name="the-filter-pane-on-the-on-hand-list-page-doesnt-work-as-expected"></a>لا يعمل جزء التصفية على صفحة القائمة الفعلية كما هو متوقع

## <a name="symptoms"></a>العلامات

لا تقوم عوامل التصفية في جزء التصفية الموجود في الصفحة **القائمة الفعلية**  بتصفية النتائج كما تتوقعها.

## <a name="resolution"></a>الحل

يتم تجميع صفحة  **قائمة المخزون الفعلي**  من جدول المخزون الفعلي الذي يتضمن جميع الأبعاد المتوفرة. ومع ذلك، القائمة الموجودة في هذه الصفحة هي ملخص. وبالتالي، فقد تجمع الصفوف من الجدول المصدر عن طريق تجميع القيم وفقًا للأبعاد المعروضة.

عوامل التصفية التي تم إعدادها في جزء عوامل التصفية على الجدول المصدر، وليس على القائمة المجمعة. قد يؤدي هذا السلوك في بعض الأحيان إلى ظهور نتائج غير متوقعه، كما هو موضح في [الامثله التالية](/dynamics365/supply-chain/inventory/inventory-on-hand-list.md#examples).

ومع ذلك، فإن  [عوامل التصفية المتوفرة في الشبكة](/dynamics365/supply-chain/inventory/inventory-on-hand-list.md#grid-filters) *تنطبق*  على القائمة المجمعة. تتضمن عوامل التصفية هذه QuickFilter في الجزء العلوي من الشبكة بالإضافة إلى عامل التصفية لكل عنوان عمود.
