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
ms.openlocfilehash: a41cf955d151726348bea83e52a24bc8784352c2d07268ced944e4cc6bf35491
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/05/2021
ms.locfileid: "6712900"
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
