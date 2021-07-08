---
title: يجب جدولة أمر الإنتاج المخطط قبل أن يتم تأكيده
description: عند محاولة تأكيد أمر مخطط، فإنك تتلقى رسالة خطأ تنص على أنه يجب جدولة الأمر قبل أن يتم تأكيده.
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
ms.openlocfilehash: a360cb3cbd26e1bc1ebb1baf1a6a4d8282c28c5c
ms.sourcegitcommit: 18ca2df785e9656fdd4e8c0734eca2b2624fda10
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/22/2021
ms.locfileid: "6294006"
---
# <a name="planned-production-order-must-be-scheduled-before-it-can-be-firmed"></a><span data-ttu-id="1d4aa-103">يجب جدولة أمر الإنتاج المخطط قبل أن يتم تأكيده</span><span class="sxs-lookup"><span data-stu-id="1d4aa-103">Planned production order must be scheduled before it can be firmed</span></span>

<span data-ttu-id="1d4aa-104">رمز الخطأ: SYS309802</span><span class="sxs-lookup"><span data-stu-id="1d4aa-104">Error code: SYS309802</span></span>

## <a name="symptoms"></a><span data-ttu-id="1d4aa-105">العلامات</span><span class="sxs-lookup"><span data-stu-id="1d4aa-105">Symptoms</span></span>

<span data-ttu-id="1d4aa-106">عند محاولة تأكيد أمر مخطط، تظهر رسالة الخطأ التالية:</span><span class="sxs-lookup"><span data-stu-id="1d4aa-106">When you try to firm a planned order, you receive the following error message:</span></span>

> <span data-ttu-id="1d4aa-107">يجب جدولة أمر الإنتاج المخطط قبل التمكن من تأكيده.</span><span class="sxs-lookup"><span data-stu-id="1d4aa-107">The planned production order must be scheduled before it can be firmed.</span></span>

## <a name="cause"></a><span data-ttu-id="1d4aa-108">السبب</span><span class="sxs-lookup"><span data-stu-id="1d4aa-108">Cause</span></span>

<span data-ttu-id="1d4aa-109">لا يمكن أن يكون تواريخ البدء والانتهاء المجدولة فارغة.</span><span class="sxs-lookup"><span data-stu-id="1d4aa-109">The scheduled start and end dates can't be blank.</span></span>

## <a name="resolution"></a><span data-ttu-id="1d4aa-110">الحل</span><span class="sxs-lookup"><span data-stu-id="1d4aa-110">Resolution</span></span>

<span data-ttu-id="1d4aa-111">لتحديد تواريخ البدء والانتهاء للأمر المخطط، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="1d4aa-111">To specify start and end dates for the planned order, follow these steps.</span></span>

1. <span data-ttu-id="1d4aa-112">انتقل إلى **التخطيط الرئيسي \> التخطيط الرئيسي \> الطلبات المخططة**.</span><span class="sxs-lookup"><span data-stu-id="1d4aa-112">Go to **Master planning \> Master planning \> Planned orders**.</span></span>
1. <span data-ttu-id="1d4aa-113">افتح الأمر المخطط المتعلق.</span><span class="sxs-lookup"><span data-stu-id="1d4aa-113">Open the relevant planned order.</span></span>
1. <span data-ttu-id="1d4aa-114">في علامة التبويب السريعة **عام**، في القسم **مجدول**، حدد التواريخ في الحقلين **تاريخ البدء** و **تاريخ الانتهاء**.</span><span class="sxs-lookup"><span data-stu-id="1d4aa-114">On the **General** FastTab, in the **Scheduled** section, specify dates in the **Start date** and **End date** fields.</span></span>
