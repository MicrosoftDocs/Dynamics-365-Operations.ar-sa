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
ms.openlocfilehash: 970930bbdd30b57a8374de7810bb3ece8cb19a7010b5ef19d90bfc39d09f172b
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/05/2021
ms.locfileid: "6740541"
---
# <a name="the-warehouse-in-the-picking-list-journal-isnt-updated-on-a-bom-line"></a>لا يتم تحديث المستودع الموجود في دفتر يومية قائمة الانتقاء في بند قائمة مكونات الصنف

رقم KB: 4614848

## <a name="symptoms"></a>العلامات

لا يتم تحديث المستودع الموجود في دفتر يومية قائمة الانتقاء في بند قائمة مكونات الصنف (BOM).

## <a name="resolution"></a>الدقة

يعمل النظام كما هو مصمم. في حالة إنشاء بند دفتر يومية قائمة الانتقاء الذي يحتوي على مرجع (بواسطة معرف الدفعة) إلى بند قائمة مكونات الصنف‬، لن يتم تحديث المستودع الموجود في بند قائمة مكونات الصنف‬ إذا تم تغيير بعد المستودع الموجود في بند دفتر يومية قائمة انتقاء الإنتاج في وقت لاحق.
