---
title: لا يمكنك تحديث تكلفة الوحدة المتوقعة عند استيراد سجلات التنبؤ بالطلب
description: عند استخدام كيانات بيانات لاستيراد سجلات التنبؤ بالطلب، لا يتم تحديث سعر التكلفة للسجلات الموجودة بحيث يتوافق مع البيانات المستوردة.
author: ChristianRytt
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: DataManagementWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: angarmas
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: c8ea8322a6c7bafe2dfcaaee3e9989f753c85e2a
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026239"
---
# <a name="you-cant-update-the-forecasted-unit-cost-when-you-import-demand-forecast-records"></a>لا يمكنك تحديث تكلفة الوحدة المتوقعة عند استيراد سجلات التنبؤ بالطلب

رقم KB: 4614109

## <a name="symptoms"></a>العلامات

عند استخدام كيانات بيانات لاستيراد سجلات التنبؤ بالطلب، لا يتم تحديث قيمة **تكلفة الوحدة المتوقعة** للسجلات الموجودة بحيث يتوافق مع البيانات المستوردة.

## <a name="cause"></a>السبب

**تكلفة الوحدة المتوقعة** عبارة عن حقل للقراءة فقط. تعتمد القيمة على تكلفة وحدة المنتج ولا يمكن تعيينها بشكل مباشر من خلال عملية الاستيراد.

## <a name="resolution"></a>الدقة

ونظرًاا لأن الحقل للقراءة فقط، لا يمكن استيراد القيم له. سيتم حساب القيمة وفقًا لمنطق الأعمال الموجود.
