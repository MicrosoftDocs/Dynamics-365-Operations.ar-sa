---
title: تنطبق حالات سير عمل دفتر يومية المخزون على مستوى دفتر اليومية وليس على مستوى البند
description: تنطبق حالات سير عمل دفتر يومية المخزون فقط على مستوى دفتر اليومية، وليس عند مستوي البند.
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
ms.openlocfilehash: 46bdde7f09c639fbefd46162431762b056d521ae
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475471"
---
# <a name="inventory-journal-workflow-conditions-apply-at-the-journal-level-not-line-level"></a>تنطبق حالات سير عمل دفتر يومية المخزون على مستوى دفتر اليومية وليس على مستوى البند

## <a name="symptoms"></a>العلامات

قد تواجهك هذه المشكلة في حاله قيامك، علي سبيل المثال، بمحاولة اعداد شرط سير عمل "دفتر يوميه المخزون" علي مبلغ التكلفة. قم باعداد الشرط بحيث يتم تشغيل الخطوة 1 فقط عندما يكون مبلغ التكلفة اقل من 100. قم باعداد شرط آخر بحيث يتم تشغيل الخطوة 2 فقط عندما يكون مبلغ التكلفة أكثر من أو يساوي 100. وبعد ذلك، عند تشغيل سير العمل، تظهر محفوظات سير العمل بندا واحدا فقط، ويتم دائما تقييم الشرط الأول علي انه *صواب*، بغض النظر عن القيمة التي يتم إرسالها.

## <a name="workaround"></a>حل بديل

في الإصدار الحالي، تنطبق شروط سير عمل دفتر يوميه المخزون فقط علي مستوي دفتر اليومية، وليس عند مستوي البند. يتم هذا السلوك بسبب التصميم. نوصي بتعيين معايير الشرط فقط في السمات علي مستوي دفتر اليومية.
