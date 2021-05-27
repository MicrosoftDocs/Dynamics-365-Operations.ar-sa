---
title: حساب TDS على الحركات بين الشركات الشقيقة
description: يصف هذا الموضوع العملية المستخدمة لحساب الضريبة المخصومة في المصدر (TDS) على الحركات بين الشركات الشقيقة على مراحل.
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: 0e304747cc93bfe0a39beababc3182ca14664b11
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023001"
---
# <a name="tds-calculation-on-intercompany-transactions"></a><span data-ttu-id="cc30d-103">حساب TDS على الحركات بين الشركات الشقيقة</span><span class="sxs-lookup"><span data-stu-id="cc30d-103">TDS calculation on intercompany transactions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="cc30d-104">يصف هذا الموضوع العملية المستخدمة لحساب الضريبة المخصومة في المصدر (TDS) على الحركات بين الشركات الشقيقة على مراحل.</span><span class="sxs-lookup"><span data-stu-id="cc30d-104">This topic describes the process that is used to calculate Tax Deducted at Source (TDS) on intercompany transactions in phases.</span></span>

<span data-ttu-id="cc30d-105">عند إنشاء أمر شراء بين الشركات الشقيقة أو أمر مبيعات، يتم استخدام مجموعة TDS الافتراضية المحددة للعميل أو المورد لحساب مبلغ TDS.</span><span class="sxs-lookup"><span data-stu-id="cc30d-105">When an intercompany purchase order or sales order is created, the default TDS group that is defined for the customer or vendor is used to calculate the TDS amount.</span></span> <span data-ttu-id="cc30d-106">يتم ترحيل مبلغ TDS إلى حسابات قابلة للاسترداد أو حسابات مستحقة الدفع بعد ترحيل الفاتورة.</span><span class="sxs-lookup"><span data-stu-id="cc30d-106">The TDS amount is posted to the recoverable or payable accounts after the invoice is posted.</span></span>

<span data-ttu-id="cc30d-107">يتم إنشاء أمر المبيعات أو أمر الشراء بين الشركات الشقيقة تلقائيًا لأمر الشراء أو أمر المبيعات الأصلي.</span><span class="sxs-lookup"><span data-stu-id="cc30d-107">An intercompany sales order or purchase order is automatically created for the original purchase order or sales order.</span></span> <span data-ttu-id="cc30d-108">يتم عرض مجموعة TDS الافتراضية في أمر بين الشركات الشقيقة، وبالتالي يمكن حساب TDS.</span><span class="sxs-lookup"><span data-stu-id="cc30d-108">The default TDS group is shown on the intercompany order, so that TDS can be calculated.</span></span> <span data-ttu-id="cc30d-109">يمكنك تغيير مجموعة TDS.</span><span class="sxs-lookup"><span data-stu-id="cc30d-109">You can change the TDS group.</span></span> <span data-ttu-id="cc30d-110">لا يمكن ترحيل الفاتورة إلا إذا كان صافي مبلغ الفاتورة في أمر بين الشركات الشقيقة الذي يتم إنشاؤه تلقائيًا يطابق صافي مبلغ الفاتورة في الأمر الأصلي.</span><span class="sxs-lookup"><span data-stu-id="cc30d-110">The invoice can be posted only if the net invoice amount on the intercompany order that is automatically created matches the net invoice amount on the original order.</span></span> <span data-ttu-id="cc30d-111">(المبلغ الصافي هو مبلغ الفاتورة بعد اقتطاع TDS.)</span><span class="sxs-lookup"><span data-stu-id="cc30d-111">(The net amount is the invoice amount after TDS is deducted.)</span></span>

<span data-ttu-id="cc30d-112">على سبيل المثال، يتم إنشاء فاتورة مبيعات بمبلغ 50.000، ويتم إرفاق TDS بنسبة **10%** بها.</span><span class="sxs-lookup"><span data-stu-id="cc30d-112">For example, a sales invoice is created for 50,000, and the **10%** TDS group is attached to it.</span></span> <span data-ttu-id="cc30d-113">ويكون مبلغ الفاتورة الذي تم ترحيله هو 45.000، ويكون مبلغ TDS الذي تم ترحيله لفاتورة المبيعات هو 5.000.</span><span class="sxs-lookup"><span data-stu-id="cc30d-113">The posted invoice amount is 45,000, and the posted TDS amount for the sales invoice is 5,000.</span></span> <span data-ttu-id="cc30d-114">ويتم إنشاء أمر الشراء تلقائيًا لأمر التوريد بين الشركات الشقيقة، ويتم إرفاق مجموعة TDS بنسبة  **10%** بها.</span><span class="sxs-lookup"><span data-stu-id="cc30d-114">A purchase order is automatically created for the intercompany sales order, and the  **10%** TDS group is attached to it.</span></span> <span data-ttu-id="cc30d-115">إذا قمت بتغيير مجموعة TDS إلى النسبة **15%**، فلن يمكنك ترحيل الفاتورة، نظرًا لأن صافي مبلغ الفاتورة لأمر المبيعات بين الشركات الشقيقة التي تم إنشاؤها تلقائيًا لا يتطابق مع صافي مبلغ فاتورة أمر المبيعات الأصلي.</span><span class="sxs-lookup"><span data-stu-id="cc30d-115">If you change the TDS group to **15%**, you can't post the invoice, because the net invoice amount of the intercompany sales order that was automatically created doesn't match the net invoice amount of the original sales order.</span></span>

<span data-ttu-id="cc30d-116">يتم ترحيل دفتر يومية المدفوعات الذي يتم إنشاؤه للفاتورة بين الشركات الشقيقة تلقائيًا.</span><span class="sxs-lookup"><span data-stu-id="cc30d-116">A payment journal that is created for an intercompany invoice is automatically posted.</span></span> <span data-ttu-id="cc30d-117">لا يمكن ترحيل دفتر يومية المدفوعات ذلك إلا إذا كان صافي مبلغ الدفع الموجود فيه يطابق صافي مبلغ الدفع في دفتر يومية المدفوعات الأصلي.</span><span class="sxs-lookup"><span data-stu-id="cc30d-117">That payment journal can be posted only if the net payment amount on it matches the net payment amount on the original payment journal.</span></span>
