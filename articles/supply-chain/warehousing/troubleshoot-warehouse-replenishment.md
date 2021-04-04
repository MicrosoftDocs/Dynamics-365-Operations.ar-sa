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
ms.openlocfilehash: 8dfb58c9156df106f58dfdc0ee2e0ef8defb9d9f
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/15/2021
ms.locfileid: "5263194"
---
# <a name="troubleshoot-warehouse-replenishment"></a><span data-ttu-id="fb214-103">استكشاف أخطاء التزويد المستودع وإصلاحها</span><span class="sxs-lookup"><span data-stu-id="fb214-103">Troubleshoot warehouse replenishment</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="fb214-104">يوضح هذا الموضوع كيفية إصلاح المشكلات الشائعة التي قد تواجهها أثناء العمل مع عمليات تزويد المستودعات في Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="fb214-104">This topic describes how to fix common issues that you might encounter while you work with warehouse replenishment in Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="i-receive-the-following-error-message-work-1-cannot-be-unblocked-because-it-has-unfinished-replenishment-work"></a><span data-ttu-id="fb214-105">أتلقى رسالة التحذير التالية: "لا يمكن إلغاء حظر معرف العمل %1 بسبب وجود عمل تزويد غير منجز."</span><span class="sxs-lookup"><span data-stu-id="fb214-105">I receive the following error message: "Work %1 cannot be unblocked because it has unfinished replenishment work."</span></span>

### <a name="issue-description"></a><span data-ttu-id="fb214-106">وصف المشكلة</span><span class="sxs-lookup"><span data-stu-id="fb214-106">Issue description</span></span>

<span data-ttu-id="fb214-107">يتم حظر عمل الانتقاء نظرا لعمل التزويد التابع.</span><span class="sxs-lookup"><span data-stu-id="fb214-107">Picking work is blocked because of dependent replenishment work.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="fb214-108">حل المشكلة</span><span class="sxs-lookup"><span data-stu-id="fb214-108">Issue resolution</span></span>

<span data-ttu-id="fb214-109">عند استخدام التزويد طلب الموجه، إذا كان من الضروري ان يكون هناك موقع انتقاء تزويدها لاستيفاء طلب المصدر ، يقوم النظام بإنشاء كل من اعمال التزويد وعمل الانتقاء.</span><span class="sxs-lookup"><span data-stu-id="fb214-109">When you use wave demand replenishment, if a picking location must be replenished to fulfill the source order demand, the system creates both the replenishment work and the picking work.</span></span> <span data-ttu-id="fb214-110">ومع ذلك ، فانه يقوم بحظر عمل الانتقاء حتى يكتمل عمل التزويد.</span><span class="sxs-lookup"><span data-stu-id="fb214-110">However, it blocks the picking work until the replenishment work is completed.</span></span> <span data-ttu-id="fb214-111">يعتبر هذا السلوك مقصودا ، لان موقع الانتقاء لن يكون له مخزون كاف الا إذا اكتمل عمل التزويد.</span><span class="sxs-lookup"><span data-stu-id="fb214-111">This behavior is intentional, because the picking location won't have enough inventory unless the replenishment work is completed.</span></span> <span data-ttu-id="fb214-112">قم بإكمال عمل التزويد، ثم قم بمعالجه عمل الانتقاء.</span><span class="sxs-lookup"><span data-stu-id="fb214-112">Complete the replenishment work, and then process the picking work.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]