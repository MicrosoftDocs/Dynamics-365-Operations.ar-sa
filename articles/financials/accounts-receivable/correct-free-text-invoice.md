---
title: "تصحيح فاتورة النص الحر"
description: "توضح هذه المقالة كيفية تصحيح فاتورة نص حر تم ترحيلها وإعادة إصدارها كفاتورة مصححة."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CustFreeInvoice
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 13991
ms.assetid: 2a0a4789-8619-4974-bef9-0923cc848420
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: cbae4c444db29a8dc7f3040aa78e45c0da092efd
ms.contentlocale: ar-sa
ms.lasthandoff: 11/03/2017

---

# <a name="correct-a-free-text-invoice"></a><span data-ttu-id="b0cd9-103">تصحيح فاتورة النص الحر</span><span class="sxs-lookup"><span data-stu-id="b0cd9-103">Correct a free text invoice</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="b0cd9-104">توضح هذه المقالة كيفية تصحيح فاتورة نص حر تم ترحيلها وإعادة إصدارها كفاتورة مصححة.</span><span class="sxs-lookup"><span data-stu-id="b0cd9-104">This article explains how to correct a free text invoice that has been posted and reissue it as a corrected invoice.</span></span>

<span data-ttu-id="b0cd9-105">‏‫لتصحيح فاتورة نص حر تم ترحيلها، افتح فاتورة النص الحر المرّحلة.</span><span class="sxs-lookup"><span data-stu-id="b0cd9-105">To correct a free text invoice that has already been posted, open the posted free text invoice.</span></span> <span data-ttu-id="b0cd9-106">وفي صفحة **الفاتورة**، حدد **إلغاء**، ثم **‬‏‫تصحيح الفاتورة**.</span><span class="sxs-lookup"><span data-stu-id="b0cd9-106">On the **Invoice** page, select **Cancel**, and then select **Correct invoice**.</span></span> <span data-ttu-id="b0cd9-107">وحدد كود سبب، وأضف التعليقات، وحدد تاريخ الفاتورة المصححة الجديدة.</span><span class="sxs-lookup"><span data-stu-id="b0cd9-107">Select a reason code, add comments, and select the date for new corrected invoice.</span></span> <span data-ttu-id="b0cd9-108">ويمكنك تعديل الفاتورة المصححة وتعديلها.</span><span class="sxs-lookup"><span data-stu-id="b0cd9-108">You can modify the corrected invoice, and post it.</span></span> 

<span data-ttu-id="b0cd9-109">وعندما تقوم بترحيل فاتورة مصححة، يتم إنشاء فاتورة إلغاء لمبلغ ائتمان يساوي مبلغ الفاتورة الأصلية.</span><span class="sxs-lookup"><span data-stu-id="b0cd9-109">When you post the corrected invoice, a canceling invoice is created for a credit amount that equals the original invoice amount.</span></span> <span data-ttu-id="b0cd9-110">ولذلك، يكون الرصيد المُجمَع للفاتورة الأصلية وفاتورة الإلغاء 0 (صفر).</span><span class="sxs-lookup"><span data-stu-id="b0cd9-110">Therefore, the combined balance of the original invoice and the canceling invoice is 0 (zero).</span></span> <span data-ttu-id="b0cd9-111">وتتم تسوية فاتورة الإلغاء مقابل الفاتورة الأصلية.</span><span class="sxs-lookup"><span data-stu-id="b0cd9-111">The canceling invoice is settled against the original invoice.</span></span> 

<span data-ttu-id="b0cd9-112">وبعد ترحيل الفاتورة المصححة، سيكون لديك ثلاث فواتير:</span><span class="sxs-lookup"><span data-stu-id="b0cd9-112">After you post the corrected invoice, you will have three invoices:</span></span>

-   <span data-ttu-id="b0cd9-113">**الفاتورة الأصلية** – الفاتورة التي تشتمل على المعلومات التي تقوم بتصحيحها.</span><span class="sxs-lookup"><span data-stu-id="b0cd9-113">**Original invoice** – The invoice that includes the information that you're correcting.</span></span>
-   <span data-ttu-id="b0cd9-114">**فاتورة الإلغاء** – فاتورة الائتمان التي تم إنشاؤها بواسطة النظام، والتي تم إنشاؤها لإلغاء أحدث فاتورة تم تصحيحها.</span><span class="sxs-lookup"><span data-stu-id="b0cd9-114">**Canceling invoice** – The system-generated credit invoice that was created to cancel the invoice that was most recently corrected.</span></span>
-   <span data-ttu-id="b0cd9-115">**الفاتورة المصححة** – الفاتورة التي تحتوي على معلومات الفاتورة التي تم تصحيحها.</span><span class="sxs-lookup"><span data-stu-id="b0cd9-115">**Corrected invoice** – The invoice that contains the corrected invoice information.</span></span>

<span data-ttu-id="b0cd9-116">يمكنك تحديد إلغاء وتصحيح الفواتير بطريقتين:</span><span class="sxs-lookup"><span data-stu-id="b0cd9-116">You can identify canceling and correcting invoices in two ways:</span></span>

-   <span data-ttu-id="b0cd9-117">تشتمل صفحة **كافة الفواتير ذات النص الحر** على عمود **التصحيح**، حيث يمكنك أن تشاهد الفواتير التي هي فواتير الإلغاء وفواتير التصحيح.</span><span class="sxs-lookup"><span data-stu-id="b0cd9-117">The **All free text invoices** page includes a **Correction** column, where you can see which invoices are canceling invoices and corrected invoices.</span></span>
-   <span data-ttu-id="b0cd9-118">يعرض رأس فاتورة النص الحر حالة **فاتورة الإلغاء '\[رقم الفاتورة\]'** أو **الفاتورة المصححة '\[رقم الفاتورة\]'**.</span><span class="sxs-lookup"><span data-stu-id="b0cd9-118">The header of the free text invoice shows a status of **Cancelling invoice '\[invoice number\]'** or **Corrected invoice '\[invoice number\]'**.</span></span>

> [!NOTE]
> <span data-ttu-id="b0cd9-119">لا تتوفر هذه الميزة إلا في حالة تحديد مفتاح تكوين **تصحيح فاتورة النص الحر**.</span><span class="sxs-lookup"><span data-stu-id="b0cd9-119">This feature is available only if the **Free text invoice correction** configuration key is selected.</span></span>




