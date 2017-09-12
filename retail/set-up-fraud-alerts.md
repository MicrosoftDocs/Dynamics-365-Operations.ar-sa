---
title: "إعداد تنبيهات الاحتيال"
description: "يشرح هذا الموضوع كيفية إعداد قواعد لتنبيه ممثلي خدمة العملاء بمعلومات الاحتيال المحتمل عند معالجة الأوامر. يمكنك تعريف رموز محددة لاستخدامها لوضع الأوامر المشبوهة قيد الانتظار تلقائيًا أو يدويًا."
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 79103
ms.assetid: e342af8d-7498-4d20-8483-ab368429c578
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: Human Translation
ms.sourcegitcommit: 20d28e22e4e89d0d864a0cbeaadeb568e73e223e
ms.openlocfilehash: 09d80015298c3d0219b6ffb290dc456990536a62
ms.contentlocale: ar-sa
ms.lasthandoff: 06/29/2017



---

# <a name="set-up-fraud-alerts"></a><span data-ttu-id="81126-104">إعداد تنبيهات الاحتيال</span><span class="sxs-lookup"><span data-stu-id="81126-104">Set up fraud alerts</span></span>

[!include[banner](includes/banner.md)]


<span data-ttu-id="81126-105">يشرح هذا الموضوع كيفية إعداد قواعد لتنبيه ممثلي خدمة العملاء بمعلومات الاحتيال المحتمل عند معالجة الأوامر.</span><span class="sxs-lookup"><span data-stu-id="81126-105">This topic explains how to set up rules to alert customer service representatives of potentially fraudulent information when orders are processed.</span></span> <span data-ttu-id="81126-106">يمكنك تعريف رموز محددة لاستخدامها لوضع الأوامر المشبوهة قيد الانتظار تلقائيًا أو يدويًا.</span><span class="sxs-lookup"><span data-stu-id="81126-106">You can define specific codes to use to automatically or manually put suspicious orders on hold.</span></span> 

<span data-ttu-id="81126-107">قبل إعداد قواعد التحقق من الاحتيال واستخدامها، يجب تمكين التحقق من الاحتيال وتعريف قيم التحقق من الاحتيال الأساسية في معلمات مراكز الاتصال.</span><span class="sxs-lookup"><span data-stu-id="81126-107">Before you set up and use fraud checking rules, you must enable fraud checking and define the basic fraud checking values in the call center parameters.</span></span> <span data-ttu-id="81126-108">وهناك نوعان من قواعد الاحتيال:</span><span class="sxs-lookup"><span data-stu-id="81126-108">There are two types of fraud rules:</span></span>

-   <span data-ttu-id="81126-109">**قواعد ثابتة** تستخدم قيمة معينة، مثل رقم هاتف تم إدراجه في القائمة السوداء.</span><span class="sxs-lookup"><span data-stu-id="81126-109">**Static rules** use a specific value, such as a phone number that has been blacklisted.</span></span>
-   <span data-ttu-id="81126-110">**القواعد الحيوية** يمكن أن تتألف من الشروط والمتغيرات.</span><span class="sxs-lookup"><span data-stu-id="81126-110">**Dynamic rules** can be composed from variables and conditions.</span></span>

<span data-ttu-id="81126-111">قبل إنشاء قاعدة ديناميكية، يجب إنشاء المتغيرات والشروط التي تعرّف من الذي يتم تطبيق القاعدة عليه ومتى يجب تطبيق القاعدة.</span><span class="sxs-lookup"><span data-stu-id="81126-111">Before you create a dynamic rule, you must create the variables and conditions that define who the rule applies to and when the rule should be applied.</span></span> <span data-ttu-id="81126-112">على سبيل المثال، تريد إنشاء قاعدة تتطلب بأنه عندما يضع العميل 1202 أمر مبيعات بقيمة 1,000.00 أو أكثر، يجب وضع أمر المبيعات قيد الانتظار حتى يتم التحقق من دفع العميل.</span><span class="sxs-lookup"><span data-stu-id="81126-112">For example, you want to create a rule to require that any sales order that customer 1202 places that is worth 1,000.00 or more be put on hold until the customer payment can be verified.</span></span> <span data-ttu-id="81126-113">وفي هذه الحالة، المتغيرات هي العميل 1202 وإجمالي الأمر 1,000.00.</span><span class="sxs-lookup"><span data-stu-id="81126-113">In this case, the variables are customer 1202 and an order total of 1,000.00.</span></span> <span data-ttu-id="81126-114">يحدد الشرط أنه إذا قدم العميل 1202 أمرًا، وكان المبلغ الإجمالي للأمر يساوي أو أكثر من 1,000.00، فيجب تعليق أمر المبيعات حتى يتم التحقق من دفع العميل.</span><span class="sxs-lookup"><span data-stu-id="81126-114">The condition specifies that if customer 1202 places an order, and the total amount of the order is equal to or more than 1,000.00, the sales order must be put on hold until the customer payment can be verified.</span></span>




