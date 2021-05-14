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
# <a name="work-isnt-blocked"></a><span data-ttu-id="227e8-103">العمل غير محظور</span><span class="sxs-lookup"><span data-stu-id="227e8-103">Work isn't blocked</span></span>

<span data-ttu-id="227e8-104">رمز الخطأ: WHSUnblockNotBlockedWorkErrorMessage</span><span class="sxs-lookup"><span data-stu-id="227e8-104">Error code: WHSUnblockNotBlockedWorkErrorMessage</span></span>

## <a name="symptoms"></a><span data-ttu-id="227e8-105">العلامات</span><span class="sxs-lookup"><span data-stu-id="227e8-105">Symptoms</span></span>

<span data-ttu-id="227e8-106">يعرض النظام رسالة الخطأ التالية:</span><span class="sxs-lookup"><span data-stu-id="227e8-106">The system shows the following error message:</span></span>

> <span data-ttu-id="227e8-107">العمل ذو المُعرف %1 غير محظور.</span><span class="sxs-lookup"><span data-stu-id="227e8-107">Work with Id %1 is not blocked.</span></span>

## <a name="cause"></a><span data-ttu-id="227e8-108">السبب</span><span class="sxs-lookup"><span data-stu-id="227e8-108">Cause</span></span>

<span data-ttu-id="227e8-109">تم تعيين خيار **الموجة المحظورة** في الموجة إلى *لا*.</span><span class="sxs-lookup"><span data-stu-id="227e8-109">The **Blocked wave** option on the wave is set to *No*.</span></span> <span data-ttu-id="227e8-110">لا يمكن إلغاء حظر العمل لأنه غير محظور حاليًا.</span><span class="sxs-lookup"><span data-stu-id="227e8-110">The work can't be unblocked because it isn't currently blocked.</span></span>

## <a name="resolution"></a><span data-ttu-id="227e8-111">الدقة</span><span class="sxs-lookup"><span data-stu-id="227e8-111">Resolution</span></span>

 <span data-ttu-id="227e8-112">يمكن فقط حظر العمل عند تعيين خيار **الموجة المحظورة** إلى *نعم*.</span><span class="sxs-lookup"><span data-stu-id="227e8-112">Only work where the **Blocked wave** option is set to *Yes* can be unblocked.</span></span>
