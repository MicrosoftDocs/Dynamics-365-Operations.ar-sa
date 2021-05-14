---
title: يجب أن تكون قيمة الوزن موجبة
description: يجب أن تكون قيمة الوزن موجبة
author: perlynne
ms.date: 04/15/2021
ms.topic: troubleshooting
ms.search.form: WHSContainerCloseDiag_canClose
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-05-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: dcbcde3143cb509b68b277cb7c709263e2659b5b
ms.sourcegitcommit: 5f5afb46431e1abd8fb6e92e0189914b598dc7fd
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/21/2021
ms.locfileid: "5924293"
---
# <a name="weight-must-be-positive"></a><span data-ttu-id="f1a77-103">يجب أن تكون قيمة الوزن موجبة</span><span class="sxs-lookup"><span data-stu-id="f1a77-103">Weight must be positive</span></span>

<span data-ttu-id="f1a77-104">رمز الخطأ: WeightMustBePositive</span><span class="sxs-lookup"><span data-stu-id="f1a77-104">Error code: WeightMustBePositive</span></span>

## <a name="symptoms"></a><span data-ttu-id="f1a77-105">العلامات</span><span class="sxs-lookup"><span data-stu-id="f1a77-105">Symptoms</span></span>

<span data-ttu-id="f1a77-106">يعرض النظام رسالة الخطأ التالية:</span><span class="sxs-lookup"><span data-stu-id="f1a77-106">The system shows the following error message:</span></span>

> <span data-ttu-id="f1a77-107">يجب أن تكون قيمة الوزن موجبة.</span><span class="sxs-lookup"><span data-stu-id="f1a77-107">Weight must be positive.</span></span>

## <a name="cause"></a><span data-ttu-id="f1a77-108">السبب</span><span class="sxs-lookup"><span data-stu-id="f1a77-108">Cause</span></span>

<span data-ttu-id="f1a77-109">تم تعيين حقل **الوزن الإجمالي** إلى *0* (صفر) أو قيمة سالبة.</span><span class="sxs-lookup"><span data-stu-id="f1a77-109">The **Gross Weight** field is set to *0* (zero) or a negative value.</span></span>

## <a name="resolution"></a><span data-ttu-id="f1a77-110">الدقة</span><span class="sxs-lookup"><span data-stu-id="f1a77-110">Resolution</span></span>

<span data-ttu-id="f1a77-111">لتحديد الوزن، اتبع إحدى هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="f1a77-111">To specify a weight, follow one of these steps.</span></span>

- <span data-ttu-id="f1a77-112">في حقل **الوزن الإجمالي**، قم بتعيين قيمة.</span><span class="sxs-lookup"><span data-stu-id="f1a77-112">In the **Gross weight** field, set a value.</span></span> <span data-ttu-id="f1a77-113">وحدد بعد ذلك وحدة في القائمة المنسدلة.</span><span class="sxs-lookup"><span data-stu-id="f1a77-113">Then select a unit in the drop-down list.</span></span>
- <span data-ttu-id="f1a77-114">حدد **الحصول على وزن النظام** لحساب قيمة **الوزن الإجمالي**.</span><span class="sxs-lookup"><span data-stu-id="f1a77-114">Select **Get system weight** to calculate the **Gross weight** value.</span></span>
