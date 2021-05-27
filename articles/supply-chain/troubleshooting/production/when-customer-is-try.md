---
title: يتم مسح رقم الدفعة عند تحديد معرف شحنة جديد
description: عندما تقوم بمراجعة بند دفتر يومية قائمة الانتقاء، فإنه يتم مسح القيمة الموجودة في الحقل رقم الدفعة إذا قمت بتحديد قيمة جديدة في الحقل معرف الشحنة.
author: johanhoffmann
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ProdJournalTransBOM
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: datra
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 71977a04adb066a8b51c9bf7b8c5a4e752ca902e
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026220"
---
# <a name="batch-number-is-cleared-when-a-new-lot-id-is-selected"></a>يتم مسح رقم الدفعة عند تحديد معرف شحنة جديد

رقم KB: 4613107

## <a name="symptoms"></a>العلامات

عندما تقوم بمراجعة بند دفتر يومية قائمة الانتقاء، فإنه يتم مسح القيمة الموجودة في الحقل **رقد الدفعة** ذا قمت بتحديد قيمة جديدة في الحقل **معرف الشحنة**.

## <a name="resolution"></a>الدقة

يعمل النظام كما هو مصمم. إذا قمت بتغيير معرف الشحنة، فإنك تقوم بتغيير سياق الصنف. ولذلك، ييتم إعادة تعيين رقم الدفعة.

لربط رقم الدفعة بمعرف شحنة، يجب تعيين معرف الشحنة أولاً.
