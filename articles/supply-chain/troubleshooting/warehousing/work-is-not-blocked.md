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
ms.openlocfilehash: 6b4361682246397732e8326b98b1b86ff878664e54c8c352296b0d7eaff6bbbd
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/05/2021
ms.locfileid: "6719541"
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
