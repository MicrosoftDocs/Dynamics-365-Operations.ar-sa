---
title: المعلمات الخاصة بالخطة الرئيسية غير موجودة
description: عند محاولة تأكيد أمر مخطط، فإنك تتلقى رسالة خطأ توضح أنه لا توجد معلمات للخطة الرئيسية.
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
ms.openlocfilehash: d4b64af2e30109b8560d40c4c532504611528bbe
ms.sourcegitcommit: 18ca2df785e9656fdd4e8c0734eca2b2624fda10
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/22/2021
ms.locfileid: "6294004"
---
# <a name="parameters-for-the-master-plan-dont-exist"></a><span data-ttu-id="af685-103">المعلمات الخاصة بالخطة الرئيسية غير موجودة</span><span class="sxs-lookup"><span data-stu-id="af685-103">Parameters for the master plan don't exist</span></span>

<span data-ttu-id="af685-104">رمز الخطأ: SYS25368</span><span class="sxs-lookup"><span data-stu-id="af685-104">Error code: SYS25368</span></span>

## <a name="symptoms"></a><span data-ttu-id="af685-105">العلامات</span><span class="sxs-lookup"><span data-stu-id="af685-105">Symptoms</span></span>

<span data-ttu-id="af685-106">عند محاولة تأكيد أمر مخطط، تظهر رسالة الخطأ التالية:</span><span class="sxs-lookup"><span data-stu-id="af685-106">When you try to firm a planned order, you receive the following error message:</span></span>

> <span data-ttu-id="af685-107">المحددات الخاصة بالخطة الرئيسية %1 غير موجودة.</span><span class="sxs-lookup"><span data-stu-id="af685-107">Parameters for master plan %1 do not exist.</span></span>

## <a name="cause"></a><span data-ttu-id="af685-108">السبب</span><span class="sxs-lookup"><span data-stu-id="af685-108">Cause</span></span>

<span data-ttu-id="af685-109">ونظرًا لمشكلات التكوين، يتعذر على النظام العثور على إعدادات الخطة المحددة.</span><span class="sxs-lookup"><span data-stu-id="af685-109">Because of configuration issues, the system can't find the settings for the specified plan.</span></span>

## <a name="resolution"></a><span data-ttu-id="af685-110">الحل</span><span class="sxs-lookup"><span data-stu-id="af685-110">Resolution</span></span>

- <span data-ttu-id="af685-111">انتقل إلى **التخطيط الرئيسي \> الإعداد \> الخطط \> الخطط الرئيسية**، وتأكد من وجود الخطة التي لها الاسم المحدد.</span><span class="sxs-lookup"><span data-stu-id="af685-111">Go to **Master planning \> Setup \> Plans \> Master plans**, and make sure that a plan that has the specified name exists.</span></span>
