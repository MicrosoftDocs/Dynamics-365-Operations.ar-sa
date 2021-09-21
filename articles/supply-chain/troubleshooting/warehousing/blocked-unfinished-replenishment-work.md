---
title: انتقاء عمل محظور بسبب عمل التزويد غير المنتهي
description: قد يتم حظر عمل الانتقاء نظراً لعمل التزويد التابع. قم بإكمال عمل التزويد ثم قم بمعالجة عمل الانتقاء.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 53b50d1e3e2d7bb64e78514affe80076ddcb9052
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475518"
---
# <a name="picking-work-cant-be-unblocked-because-of-unfinished-replenishment-work"></a>لا يمكن إلغاء حظر العمل الخاص بالانتقاء بسبب عمل التزويد غير المنتهي

## <a name="symptoms"></a>العلامات

عند استخدام تزويد طلبات الموجة، يمكن حظر انتقاء العمل بسبب عمل التزويد التابع. إذا كان من الضروري تزويد موقع انتقاء لاستيفاء طلب المصدر، فسيقوم النظام بإنشاء كل من عمل التزويد وعمل الانتقاء. ومع ذلك، فإنه يقوم بحظر عمل الانتقاء حتى يكتمل عمل التزويد وتظهر رسالة الخطأ التالية:

> لا يمكن إلغاء حظر العمل %1 لأنه يشتمل على عمل تزويد غير مكتمل.

## <a name="resolution"></a>الحل

يعتبر هذا السلوك مقصوداً، لان موقع الانتقاء لن يكون له مخزون كاف إلا إذا اكتمل عمل التزويد. قم بإكمال عمل التزويد ثم قم بمعالجة عمل الانتقاء.
