---
title: قطع اتصال عميل
description: يتناول هذا المقال ما يتعين عليك القيام به إذا تم قطع اتصال العميل من البيئة ولا يعرف السبب.
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: fcb7e5e3230aee9f6c04e4854c8eea836ae14c7f
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/18/2021
ms.locfileid: "6053409"
---
# <a name="client-disconnects"></a><span data-ttu-id="879e1-103">قطع اتصال العميل</span><span class="sxs-lookup"><span data-stu-id="879e1-103">Client disconnects</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="879e1-104">**تفاصيل البيئة**</span><span class="sxs-lookup"><span data-stu-id="879e1-104">**Environment details**</span></span> 

<span data-ttu-id="879e1-105">قد تحدث هذه المشكلة في كافة البيئات.</span><span class="sxs-lookup"><span data-stu-id="879e1-105">This issue can occur in all environments.</span></span>
 
<span data-ttu-id="879e1-106">**العَرَضْ**</span><span class="sxs-lookup"><span data-stu-id="879e1-106">**Symptom**</span></span> 

<span data-ttu-id="879e1-107">تم قطع اتصال العميل من البيئة ولا يعرف السبب.</span><span class="sxs-lookup"><span data-stu-id="879e1-107">The customer is disconnected from the environment and doesn't know why.</span></span> <span data-ttu-id="879e1-108">يظهر أمام العميل واحدة من رسالتي الخطأ التاليتين:</span><span class="sxs-lookup"><span data-stu-id="879e1-108">The customer receives one of the following error messages:</span></span>

- <span data-ttu-id="879e1-109">فُقد اتصالك.</span><span class="sxs-lookup"><span data-stu-id="879e1-109">We've lost your connection.</span></span> <span data-ttu-id="879e1-110">انقر فوق إغلاق لمتابعة العمل.</span><span class="sxs-lookup"><span data-stu-id="879e1-110">Click Close to continue working.</span></span>
- <span data-ttu-id="879e1-111">يبدو أنك فقدت اتصالك بالشبكة، انقر فوق "إعادة المحاولة" للمحاولة مرة أخرى.</span><span class="sxs-lookup"><span data-stu-id="879e1-111">It appears you lost network connectivity, click Retry to try again.</span></span>

<span data-ttu-id="879e1-112">**علامة حمراء**</span><span class="sxs-lookup"><span data-stu-id="879e1-112">**Red flag**</span></span>

<span data-ttu-id="879e1-113">تحدث هذه المشكلة عادةً عندما يكون المستخدمون في مرحلة التنفيذ وعندما يقومون بمقارنة المعلومات عبر بيئات الإنتاج والاختبار، ولا يتذكروا أنهم يتنقلون بين جلسات العمل.</span><span class="sxs-lookup"><span data-stu-id="879e1-113">This issue often occurs when users are in the implementation stage, are comparing information across production and test environments, and forget that they are moving between sessions.</span></span> <span data-ttu-id="879e1-114">إذا كان المستخدمون في هذه المرحلة، فسوف يواجهون على الأرجح هذه المشكلة.</span><span class="sxs-lookup"><span data-stu-id="879e1-114">If users are at this stage, they will most likely experience this issue.</span></span>

<span data-ttu-id="879e1-115">**إصدار**</span><span class="sxs-lookup"><span data-stu-id="879e1-115">**Issue**</span></span> 

<span data-ttu-id="879e1-116">**أنواع المستعرضات:** Google Chrome وInternet Explorer وMicrosoft Edge</span><span class="sxs-lookup"><span data-stu-id="879e1-116">**Browser types:** Google Chrome, Internet Explorer, and Microsoft Edge</span></span>

<span data-ttu-id="879e1-117">يقطع Microsoft Dynamics 365 Human Resources اتصال المستخدمين عندما يتم فتح جلستي عمل مختلفتين في نفس الوقت لنفس المستخدم وعلى نفس نوع المستعرض.</span><span class="sxs-lookup"><span data-stu-id="879e1-117">Microsoft Dynamics 365 Human Resources disconnects users when two different sessions are open at the same time for the same user and the same browser type.</span></span> <span data-ttu-id="879e1-118">(على سبيل المثال، يقوم مستخدم أ بعرض البيئة 1 والبيئة 2 في مستعرض Chrome.) لا يهم إذا ما كان المستخدمين يفتحون نوافذ مستعرض مختلفة أو علامات تبويب مختلفة.</span><span class="sxs-lookup"><span data-stu-id="879e1-118">(For example, user A is viewing both environment 1 and environment 2 in Chrome.) It doesn't matter whether the users open different browser windows or different tabs.</span></span> <span data-ttu-id="879e1-119">إذا استخدمت نفس بيانات اعتماد المستخدم لتسجيل الدخول إلى كل من البيئة 1 والبيئة 2 في نفس الوقت وفي نفس نوع المستعرض، فسوف يقوم Human Resources بقطع اتصال إحدى الجلسات.</span><span class="sxs-lookup"><span data-stu-id="879e1-119">If the same user credentials are used to sign in to both environment 1 and environment 2 at the same time and in the same browser type, Human Resources disconnects one of the sessions.</span></span>

<span data-ttu-id="879e1-120">**الحل**</span><span class="sxs-lookup"><span data-stu-id="879e1-120">**Solution**</span></span>

<span data-ttu-id="879e1-121">تأكد من فتح بيئة واحدة فقط في كل مرة لنوع مستعرض معين.</span><span class="sxs-lookup"><span data-stu-id="879e1-121">Make sure that only one environment is open at a time for a given browser type.</span></span> <span data-ttu-id="879e1-122">يمكن للمستخدمين فتح جلسات متعددة لنفس البيئة (بمعني، علامات تبويب متعددة في نفس المستعرض).</span><span class="sxs-lookup"><span data-stu-id="879e1-122">Users can open multiple sessions to the same environment (that is, multiple tabs in the same browser).</span></span>

<span data-ttu-id="879e1-123">يجب على المستخدمين الذين يريدون الانتقال بين اثنين من البيئات في نفس الوقت فتح كل بيئة في نوع مستعرض مختلف.</span><span class="sxs-lookup"><span data-stu-id="879e1-123">Users who want to jump between two environments at the same time should open each environment in a different browser type.</span></span> <span data-ttu-id="879e1-124">(على سبيل المثال، بإمكان المستخدم أ عرض البيئة 1 في Chrome والبيئة 2 في Microsoft Edge.)</span><span class="sxs-lookup"><span data-stu-id="879e1-124">(For example, user A can view environment 1 in Chrome and environment 2 in Microsoft Edge.)</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]