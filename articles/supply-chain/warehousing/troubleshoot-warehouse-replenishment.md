---
title: استكشاف أخطاء استعاضة المستودع وإصلاحها
description: يوضح هذا الموضوع كيفية إصلاح المشكلات الشائعة التي قد تواجهها أثناء العمل مع عمليات تزويد المستودعات في Microsoft Dynamics 365 Supply Chain Management.
author: perlynne
manager: tfehr
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 7748a18d2b6f612b3ac9ac1a75efb6ae5f13859a
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/15/2021
ms.locfileid: "4993846"
---
# <a name="troubleshoot-warehouse-replenishment"></a>استكشاف أخطاء التزويد المستودع وإصلاحها

[!include [banner](../includes/banner.md)]

يوضح هذا الموضوع كيفية إصلاح المشكلات الشائعة التي قد تواجهها أثناء العمل مع عمليات تزويد المستودعات في Microsoft Dynamics 365 Supply Chain Management.

## <a name="i-receive-the-following-error-message-work-1-cannot-be-unblocked-because-it-has-unfinished-replenishment-work"></a>أتلقى رسالة التحذير التالية: "لا يمكن إلغاء حظر معرف العمل %1 بسبب وجود عمل تزويد غير منجز."

### <a name="issue-description"></a>وصف المشكلة

يتم حظر عمل الانتقاء نظرا لعمل التزويد التابع.

### <a name="issue-resolution"></a>حل المشكلة

عند استخدام التزويد طلب الموجه، إذا كان من الضروري ان يكون هناك موقع انتقاء تزويدها لاستيفاء طلب المصدر ، يقوم النظام بإنشاء كل من اعمال التزويد وعمل الانتقاء. ومع ذلك ، فانه يقوم بحظر عمل الانتقاء حتى يكتمل عمل التزويد. يعتبر هذا السلوك مقصودا ، لان موقع الانتقاء لن يكون له مخزون كاف الا إذا اكتمل عمل التزويد. قم بإكمال عمل التزويد، ثم قم بمعالجه عمل الانتقاء.
