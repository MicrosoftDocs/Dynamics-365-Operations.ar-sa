---
title: لم تتم الموافقة على رقم المعادلة المحدد لأمر الدفعة
description: عند محاولة تأكيد أمر مخطط، تتلقى رسالة خطأ تنص على عدم الموافقة على رقم المعادلة المحدد لأمر دفعي.
author: ankubik
ms.date: 06/10/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPo
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ankubik
ms.search.validFrom: 2021-06-10
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 4f993c92ca0a2f8f79e4b0e0eda43904529163f8
ms.sourcegitcommit: 18ca2df785e9656fdd4e8c0734eca2b2624fda10
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/22/2021
ms.locfileid: "6293998"
---
# <a name="selected-formula-number-isnt-approved-for-a-batch-order"></a>لم تتم الموافقة على رقم المعادلة المحدد لأمر الدفعة

رمز الخطأ: PRO2614

## <a name="symptoms"></a>العلامات

عند محاولة تأكيد أمر مخطط، تظهر رسالة الخطأ التالية:

> رقم التركيبة المحدد غير معتمَد لأمر دُفعي.

## <a name="cause"></a>السبب

يقوم النظام بالتحقق من صحة عملية التأكيد لضمان توفر صيغة معتمدة للصنف النشط. يجب أن توافق على المعادلة على الأرجح.

## <a name="resolution"></a>الحل

للموافقة على المعادلة، اتبع الخطوات التالية.

1. انتقل إلى **إدارة معلومات المنتج \> قوائم مكونات الصنف والمعادلات \> المعادلات**.
1. حدد المعادلة المناسبة.
1. في جزء الإجراءات، في علامة تبويب **المعادلة** في مجموعة **الاحتفاظ**، حدد **الموافقة على المعادلة**.
1. في مربع الحوار **الموافقة على قائمة مكونات الصنف**، حدد أحد الموافقين، ثم حدد **موافق**.
