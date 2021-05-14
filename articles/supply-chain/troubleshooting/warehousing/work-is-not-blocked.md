---
title: العمل غير محظور
description: العمل غير محظور
author: perlynne
ms.date: 04/15/2021
ms.topic: troubleshooting
ms.search.form: WHSWorkTable_WHSWorkUnblocking
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-05-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: d64ab282972e46e8857581b59e5705dd15667328
ms.sourcegitcommit: 5f5afb46431e1abd8fb6e92e0189914b598dc7fd
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/21/2021
ms.locfileid: "5924194"
---
# <a name="work-isnt-blocked"></a>العمل غير محظور

رمز الخطأ: WHSUnblockNotBlockedWorkErrorMessage

## <a name="symptoms"></a>العلامات

يعرض النظام رسالة الخطأ التالية:

> العمل ذو المُعرف %1 غير محظور.

## <a name="cause"></a>السبب

تم تعيين خيار **الموجة المحظورة** في الموجة إلى *لا*. لا يمكن إلغاء حظر العمل لأنه غير محظور حاليًا.

## <a name="resolution"></a>الدقة

 يمكن فقط حظر العمل عند تعيين خيار **الموجة المحظورة** إلى *نعم*.
