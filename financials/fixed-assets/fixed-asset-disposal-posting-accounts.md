---
title: "حسابات ترحيل التخلص من الأصول الثابتة"
description: "توضح هذه المقالة كيفية إعداد حسابات ترحيل دفتر الأستاذ العام للتخلص من الأصول."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AssetPosting
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 3461
ms.assetid: dfdc0730-e030-48cc-8d93-15bdc7b23776
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 20d28e22e4e89d0d864a0cbeaadeb568e73e223e
ms.openlocfilehash: 0129eae177d44100b09c2b7bce553dd5bde5ce0c
ms.contentlocale: ar-sa
ms.lasthandoff: 06/29/2017


---

# <a name="fixed-asset-disposal-posting-accounts"></a><span data-ttu-id="8a633-103">حسابات ترحيل التخلص من الأصول الثابتة</span><span class="sxs-lookup"><span data-stu-id="8a633-103">Fixed asset disposal posting accounts</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="8a633-104">توضح هذه المقالة كيفية إعداد حسابات ترحيل دفتر الأستاذ العام للتخلص من الأصول.</span><span class="sxs-lookup"><span data-stu-id="8a633-104">This article explains how to set up general ledger posting accounts for disposing of assets.</span></span>

<span data-ttu-id="8a633-105">في صفحة "ملفات تعريف ترحيل الأصول الثابتة"، في علامة التبويب السريع حسابات دفتر الأستاذ، حدد التخلص - البيع والتخلص -الخردة لإعداد عمليات الترحيل إلى دفتر الأستاذ.</span><span class="sxs-lookup"><span data-stu-id="8a633-105">In the Fixed asset posting profiles page, on the Ledger accounts FastTab, select Disposal - sale and Disposal - scrap to set up postings to the ledger.</span></span>

<span data-ttu-id="8a633-106">لكل نوع من نوعي الحركة، تتم إضافة حساب دفتر أستاذ لقيمة التخلص من الأصل الثابت.</span><span class="sxs-lookup"><span data-stu-id="8a633-106">For both transaction types, the ledger account is credited for the disposal value of the fixed asset.</span></span> <span data-ttu-id="8a633-107">ويتم ترحيل الدين إلى حساب مقابل، والذي قد يكون حسابًا بنكيًا مثلاً.</span><span class="sxs-lookup"><span data-stu-id="8a633-107">The debit is posted to an offset account, which might be, for example, a bank account.</span></span> <span data-ttu-id="8a633-108">وفي حالة بيع أصل ثابت للعميل، يتم استخدام حساب العميل بدلاً من الحساب المقابل.</span><span class="sxs-lookup"><span data-stu-id="8a633-108">If a fixed asset is sold to a customer, the customer account is used instead of the offset account.</span></span>

<span data-ttu-id="8a633-109">انقر فوق التخلص ثم انقر فوق البيع أو الخردة، ثم قم بإعداد الحسابات المفصلة لعكس صافي القيمة الدفترية للأصل الثابت.</span><span class="sxs-lookup"><span data-stu-id="8a633-109">Click Disposal and then click Sale or Scrap, and then set up detailed accounts to reverse the net book value of the fixed asset.</span></span> <span data-ttu-id="8a633-110">يمكنك أيضًا إدخال معلومات في حقلي ترحيل القيمة ونوع قيمة المبيعات في صفحة معلمات التخلص.</span><span class="sxs-lookup"><span data-stu-id="8a633-110">You can also enter information in the Post value and Sales value type fields in the Disposal parameters page.</span></span> 

<span data-ttu-id="8a633-111">تؤدي حركة التخلص من أحد الأصول في وعاء القيمة المنخفضة إلى تقليل صافي القيمة الدفترية لوعاء القيمة المنخفضة بمقدار مبلغ التخلص فقط.</span><span class="sxs-lookup"><span data-stu-id="8a633-111">The disposal transaction for an asset in a low-value pool reduces the net book value of the low-value pool by the disposed amount only.</span></span> <span data-ttu-id="8a633-112">ولكن عندما يتجاوز يكون بيع أحد الأصول صافي القيمة الدفترية لوعاء القيمة المنخفضة، فإنه يتم تقليل صافي القيمة الدفترية إلى الصفر.</span><span class="sxs-lookup"><span data-stu-id="8a633-112">However, when the sale of an asset is exceeds the net book value of the low-value pool, the net book value is reduced to zero.</span></span>






