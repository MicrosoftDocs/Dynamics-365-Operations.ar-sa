---
title: لا يمكن أن يحتوي الصنف على قائمة مكونات الصنف (BOM)‬ أو معادلة
description: عند محاولة التأكيد على أمر، فإنك تتلقى رسالة خطأ أثناء التحقق من صحة الصنف. يوضح أن الصنف لا يمكن ان قائمة مكونات الصنف (BOM) أو المعادلة.
author: ankubik
ms.date: 06/10/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPO
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ankubik
ms.search.validFrom: 2021-06-10
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 6739b8b1e4d080055a2a0501427eac1c2e8a96c5
ms.sourcegitcommit: 18ca2df785e9656fdd4e8c0734eca2b2624fda10
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/22/2021
ms.locfileid: "6294002"
---
# <a name="item-cant-have-a-bom-or-formula"></a><span data-ttu-id="b4daf-104">لا يمكن أن يحتوي الصنف على قائمة مكونات الصنف (BOM)‬ أو معادلة</span><span class="sxs-lookup"><span data-stu-id="b4daf-104">Item can't have a BOM or formula</span></span>

<span data-ttu-id="b4daf-105">رمز الخطأ: PRO2614</span><span class="sxs-lookup"><span data-stu-id="b4daf-105">Error code: PRO2614</span></span>

## <a name="symptoms"></a><span data-ttu-id="b4daf-106">العلامات</span><span class="sxs-lookup"><span data-stu-id="b4daf-106">Symptoms</span></span>

<span data-ttu-id="b4daf-107">عند محاولة التأكيد على أمر، فإنك تتلقى رسالة الخطأ التالية أثناء التحقق من صحة الصنف:</span><span class="sxs-lookup"><span data-stu-id="b4daf-107">When you try to firm an order, you receive the following error message during item validation:</span></span>

> <span data-ttu-id="b4daf-108">لا يمكن أن يحتوي الصنف على قائمة مكونات صنف أو معادلة</span><span class="sxs-lookup"><span data-stu-id="b4daf-108">Item cannot have a BOM or formula</span></span>

## <a name="resolution"></a><span data-ttu-id="b4daf-109">الحل</span><span class="sxs-lookup"><span data-stu-id="b4daf-109">Resolution</span></span>

<span data-ttu-id="b4daf-110">يجب أن تكون الأصناف التي تحتوي على قائمة مكونات الصنف (BOM) أو المعادلة من النوع *صنف التخطيط* أو *قائمة مكونات الصنف* أو *المعادلة*.</span><span class="sxs-lookup"><span data-stu-id="b4daf-110">Items that have a bill of materials (BOM) or formula must be of the *Planning item*, *BOM*, or *formula* type.</span></span> <span data-ttu-id="b4daf-111">لتغيير نوع صنف، اتبع هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="b4daf-111">To change the type of an item, follow these steps.</span></span>

1. <span data-ttu-id="b4daf-112">انتقل إلى **إدارة معلومات المنتج‬ \> المنتجات \> المنتجات الصادرة**.</span><span class="sxs-lookup"><span data-stu-id="b4daf-112">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="b4daf-113">افتح المنتج ذا الصلة.</span><span class="sxs-lookup"><span data-stu-id="b4daf-113">Open the relevant product.</span></span>
1. <span data-ttu-id="b4daf-114">في علامة التبويب السريعة **المهندس**، قم بتعيين الحقل **نوع الإنتاج** إلى *صنف التخطيط* أو *قائمة مكونات الصنف* أو *المعادلة*.</span><span class="sxs-lookup"><span data-stu-id="b4daf-114">On the **Engineer** FastTab, set the **Production type** field to *Planning item*, *BOM*, or *formula*.</span></span>
