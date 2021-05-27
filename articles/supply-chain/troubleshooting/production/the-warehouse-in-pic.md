---
title: لا يتم تحديث المستودع الموجود في دفتر يومية قائمة الانتقاء في بند قائمة مكونات الصنف.
description: لا يتم تحديث المستودع الموجود في دفتر يومية قائمة الانتقاء في بند قائمة مكونات الصنف (BOM).
author: johanhoffmann
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ProdJournalTransBOM
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 5d24c0b8538f3894fd1d2a3edb3a6ed8633c9609
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026226"
---
# <a name="the-warehouse-in-the-picking-list-journal-isnt-updated-on-a-bom-line"></a>لا يتم تحديث المستودع الموجود في دفتر يومية قائمة الانتقاء في بند قائمة مكونات الصنف

رقم KB: 4614848

## <a name="symptoms"></a>العلامات

لا يتم تحديث المستودع الموجود في دفتر يومية قائمة الانتقاء في بند قائمة مكونات الصنف (BOM).

## <a name="resolution"></a>الدقة

يعمل النظام كما هو مصمم. في حالة إنشاء بند دفتر يومية قائمة الانتقاء الذي يحتوي على مرجع (بواسطة معرف الدفعة) إلى بند قائمة مكونات الصنف‬، لن يتم تحديث المستودع الموجود في بند قائمة مكونات الصنف‬ إذا تم تغيير بعد المستودع الموجود في بند دفتر يومية قائمة انتقاء الإنتاج في وقت لاحق.
