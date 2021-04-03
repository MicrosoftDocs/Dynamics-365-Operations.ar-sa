---
title: قطع اتصال عميل
description: يتناول هذا المقال ما يتعين عليك القيام به إذا تم قطع اتصال العميل من بيئته ولا يعرف السبب.
author: andreabichsel
manager: tfehr
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 6808132e182ea6fed4fb0605fd07c008d208e89f
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/17/2021
ms.locfileid: "5468169"
---
# <a name="client-disconnects"></a>قطع اتصال عميل

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

**تفاصيل البيئة** 

قد تحدث هذه المشكلة في كافة البيئات.
 
**العَرَضْ** 

تم قطع اتصال العميل من بيئته ولا يعرف السبب. يظهر أمام العميل واحدة من رسالتي الخطأ التاليتين:

- فُقد اتصالك. انقر فوق إغلاق لمتابعة العمل.
- يبدو أنك فقدت اتصالك بالشبكة، انقر فوق "إعادة المحاولة" للمحاولة مرة أخرى.

**علامة حمراء**

تحدث هذه المشكلة عادةً عندما يكون المستخدمون في مرحلة التنفيذ وعندما يقومون بمقارنة المعلومات عبر بيئات الإنتاج والاختبار، ولا يتذكروا أنهم يتنقلون بين جلسات العمل. إذا كان المستخدمون في هذه المرحلة، فسوف يواجهون على الأرجح هذه المشكلة.

**إصدار** 

**أنواع المستعرضات:** Google Chrome وInternet Explorer وMicrosoft Edge

يقطع Microsoft Dynamics 365 Human Resources اتصال المستخدمين عندما يتم فتح جلستي عمل مختلفتين في نفس الوقت لنفس المستخدم وعلى نفس نوع المستعرض. (على سبيل المثال، يقوم مستخدم أ بعرض البيئة 1 والبيئة 2 في مستعرض Chrome.) لا يهم إذا ما كان المستخدمين يفتحون نوافذ مستعرض مختلفة أو علامات تبويب مختلفة. إذا استخدمت نفس بيانات اعتماد المستخدم لتسجيل الدخول إلى كل من البيئة 1 والبيئة 2 في نفس الوقت وفي نفس نوع المستعرض، فسوف يقوم Human Resources بقطع اتصال إحدى الجلسات.

**الحل**

تأكد من فتح بيئة واحدة فقط في كل مرة لنوع مستعرض معين. يمكن للمستخدمين فتح جلسات متعددة لنفس البيئة (بمعني، علامات تبويب متعددة في نفس المستعرض).

يجب على المستخدمين الذين يريدون الانتقال بين اثنين من البيئات في نفس الوقت فتح كل بيئة في نوع مستعرض مختلف. (على سبيل المثال، بإمكان المستخدم أ عرض البيئة 1 في Chrome والبيئة 2 في Microsoft Edge.)


[!INCLUDE[footer-include](../includes/footer-banner.md)]