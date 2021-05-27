---
title: حدث خطأ عندما تم ترحيل دفتر يومية التقرير كمنتهٍ
description: عند ترحيل دفتر يومية الإبلاغ كمنته، تظهر رسالة خطأ توضح أنه لا يمكن تخفيض الكمية المطلوبة.
author: johanhoffmann
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ProdTableListPage, ProdParameters
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 55db7d0033dd66c1b973abf96671a20ab05d61d8
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026224"
---
# <a name="error-when-the-report-as-finished-journal-is-posted"></a><span data-ttu-id="663e4-103">حدث خطأ عندما تم ترحيل دفتر يومية التقرير كمنتهٍ</span><span class="sxs-lookup"><span data-stu-id="663e4-103">Error when the Report as finished journal is posted</span></span>

<span data-ttu-id="663e4-104">رقم KB: 4612891</span><span class="sxs-lookup"><span data-stu-id="663e4-104">KB number: 4612891</span></span>

## <a name="symptoms"></a><span data-ttu-id="663e4-105">العلامات</span><span class="sxs-lookup"><span data-stu-id="663e4-105">Symptoms</span></span>

<span data-ttu-id="663e4-106">عند ترحيل دفتر اليومية **‏‫الإبلاغ كمنته**، يحدث خطأ، وتظهر رسالة الخطأ التالية:</span><span class="sxs-lookup"><span data-stu-id="663e4-106">When you post the **Report as finished** journal, an error occurs, and you receive the following error message:</span></span>

> <span data-ttu-id="663e4-107">لا يمكن تقليل الكمية المطلوبة لأنه لا توجد حركات مخزون مفتوحة كافية مع الحالة "مطلوب".</span><span class="sxs-lookup"><span data-stu-id="663e4-107">Quantity ordered cannot be reduced because there are not enough open inventory transactions with the ordered status.</span></span> <span data-ttu-id="663e4-108">يتم شراء الأصناف أو استلامها أو تسجيلها.</span><span class="sxs-lookup"><span data-stu-id="663e4-108">The items are Purchased, Received or Registered.</span></span>

<span data-ttu-id="663e4-109">يحدث هذا الخطأ فقط عند **كمية الخطأ** إلى السطر الأول من دفتر يومية **الإبلاغ كمنته** ويتم تعيين الحقل  **كمية البضائع** على السطر الأخير.</span><span class="sxs-lookup"><span data-stu-id="663e4-109">This error occurs only when the **Error quantity** field is set on the first line of the **Report as finished** journal, and the **Good quantity** field is set on the last line.</span></span> <span data-ttu-id="663e4-110">إذا تم تعيين الحقل **كمية الخطأ** في البند الأخير، لن يحدث أي خطأ.</span><span class="sxs-lookup"><span data-stu-id="663e4-110">If the **Error quantity** field is set on the last line, no error occurs.</span></span>

## <a name="resolution"></a><span data-ttu-id="663e4-111">الدقة</span><span class="sxs-lookup"><span data-stu-id="663e4-111">Resolution</span></span>

<span data-ttu-id="663e4-112">لمنع حدوث هذا الخطأ، قم بفتح الصفحة **معلمات التحكم في الإنتاج**، ثم من علامة التبويب **عام**، قم بتعيين الخيار **الكمية المتبقية بخيار كمية الخطأ** إلى *نعم*.</span><span class="sxs-lookup"><span data-stu-id="663e4-112">To prevent this error, open the **Production control parameters** page, and then, on the **General** tab, set the **Increase remain qty with error qty** option to *Yes*.</span></span>
