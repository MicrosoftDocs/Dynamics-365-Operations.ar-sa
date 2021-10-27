---
title: فشلت مهمة تنظيف محفوظات تحديث المبيعات أو انها تحتوي علي مشاكل أداء
description: قد تفشل وظيفة مجموعه التنظيف لمحفوظات المبيعات أو قد يستغرق وقتا طويلا في حاله وجود كميه كبيره من بيانات تحديث المبيعات.
author: myvakalo
ms.date: 10/05/2021
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: myvakalo
ms.search.validFrom: 2021-09-29
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 4f04dc204c705b40ed25fadc75118feaef4d6b6e
ms.sourcegitcommit: 42bd701179e664947b6eafcd1804c83a5e64abcb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/13/2021
ms.locfileid: "7641443"
---
# <a name="sales-update-history-cleanup-job-fails-or-has-performance-issues"></a>فشلت مهمة تنظيف محفوظات تحديث المبيعات أو انها تحتوي علي مشاكل أداء

## <a name="symptoms"></a>العلامات

فشلت مهمة **تنظيف محفوظات تحديث المبيعات** أو انها تحتوي علي مشاكل أداء.  

## <a name="cause"></a>السبب

يمكن ان يحدث هذا عندما يتضمن النظام الخاص بك عددا كبيرا من تحديثات المبيعات ، والذي يمكن ان ينتج عنه كميه كبيره من بيانات تحديث المبيعات. تحاول مهمة التنظيف تنظيف كافة هذه البيانات في معامله واحده. ونتيجة لذلك ، قد تتطلب الوظيفة وقتا طويلا للتشغيل أو حتى الفشل.

## <a name="resolution"></a>القرار

تتوفر نسخه جديده من مهمة مجموعه **تنظيف محفوظات تحديث المبيعات** لـ Supply Chain Management version 10.0.19 واعلي. لا يتم تمكين هذه الميزة، بشكل افتراضي. للحصول علي تفاصيل حول كيفيه عملها وكيفيه تمكينها في أداره الميزات ، راجع [تحسينات أداء تنظيف محفوظات المبيعات](../../sales-marketing/sales-update-history-cleanup-performance-improvements.md).

