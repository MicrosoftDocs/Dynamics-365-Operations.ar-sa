---
title: حسابات ترحيل الاستحواذ على الأصول الثابتة
description: توضح هذه المقالة كيفية إعداد حسابات ترحيل دفتر الأستاذ العام للاستحواذ على الأصول.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetPosting
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 23021
ms.assetid: d7e86f72-95db-4423-9b04-761e9536a959
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8fea6b1cd79b5536341a7cb50e5592ea38a7392d
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/27/2019
ms.locfileid: "2187235"
---
# <a name="fixed-asset-acquisition-posting-accounts"></a><span data-ttu-id="51c5d-103">حسابات ترحيل الاستحواذ على الأصول الثابتة</span><span class="sxs-lookup"><span data-stu-id="51c5d-103">Fixed asset acquisition posting accounts</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="51c5d-104">توضح هذه المقالة كيفية إعداد حسابات ترحيل دفتر الأستاذ العام للاستحواذ على الأصول.</span><span class="sxs-lookup"><span data-stu-id="51c5d-104">This article explains how to set up general ledger posting accounts for acquiring assets.</span></span>

<span data-ttu-id="51c5d-105">قد تختلف الحسابات المستخدمة لترحيل عمليات امتلاك الأصول الثابتة استناداً إلى الطريقة التي استُخدمت للحصول على الأصل.</span><span class="sxs-lookup"><span data-stu-id="51c5d-105">Accounts used for posting fixed asset acquisitions may vary depending upon the method used to acquire the asset.</span></span> <span data-ttu-id="51c5d-106">وفي صفحة ملفات تعريف ترحيل الأصول الثابتة، ضمن علامة التبويب حسابات دفتر الأستاذ، حدد الاستحواذ وتسوية الاستحواذ لإعداد حسابات الأصول الثابتة لترحيلها إلى دفتر الأستاذ.</span><span class="sxs-lookup"><span data-stu-id="51c5d-106">On the Fixed asset posting profiles page, on the Ledger accounts tab, select Acquisition and Acquisition adjustment to set up fixed asset accounts to post to the ledger.</span></span> 

<span data-ttu-id="51c5d-107">وفي دفاتر اليومية وأوامر الشراء، يكون حساب دفتر الأستاذ عادةً حساب الميزانية العمومية، حيث يتم خصم قيمة امتلاك الأصل الثابت الجديد.</span><span class="sxs-lookup"><span data-stu-id="51c5d-107">In journals and on purchase orders, Ledger account is typically the balance sheet account, where the acquisition value of the new fixed asset is debited.</span></span> <span data-ttu-id="51c5d-108">لا يتم عرض هذا الحساب في دفتر اليومية، ولا يمكن استبداله في الحركات.</span><span class="sxs-lookup"><span data-stu-id="51c5d-108">This account is not displayed in the journal and cannot be replaced in transactions.</span></span> 

<span data-ttu-id="51c5d-109">كما أن الحساب المقابل هو حساب ميزانية عمومية.</span><span class="sxs-lookup"><span data-stu-id="51c5d-109">Offset account is also a balance sheet account.</span></span> <span data-ttu-id="51c5d-110">وغالبًا ما سيكون هذا الحساب في دفتر اليومية العام ودفتر يومية الأصول الثابتة هو الحساب البنكي الذي يُستخدم لدفع قيمة امتلاك الأصل.</span><span class="sxs-lookup"><span data-stu-id="51c5d-110">In the general journal and in the fixed assets journal, this account often will be the bank account that is used to pay for the acquisition of the asset.</span></span> <span data-ttu-id="51c5d-111">وحساب المقابل هو حساب افتراضي يتم اقتراحه في دفاتر اليومية.</span><span class="sxs-lookup"><span data-stu-id="51c5d-111">The offset account is a default account, which is suggested in the journals.</span></span> <span data-ttu-id="51c5d-112">ويُمكن تغييره في دفتر اليومية إلى أي حساب آخر من دليل الحسابات أو إلى حساب مورّد، إذا ما تم شراء الأصول الثابتة من أحد المورّدين.</span><span class="sxs-lookup"><span data-stu-id="51c5d-112">It can be changed in the journal to any other account from the chart of accounts or to a vendor account, if the fixed asset was purchase from a vendor.</span></span> 

<span data-ttu-id="51c5d-113">في حالة استخدام دفتر يومية الفاتورة أو أوامر الشراء في الحسابات الدائنة لعمليات امتلاك الأصول الثابتة، يتم استبدال حساب المقابل لحركة الأصول الثابتة بواسطة حساب المورّد الذي تم تحديده للحركة.</span><span class="sxs-lookup"><span data-stu-id="51c5d-113">When Invoice journal or Purchase orders in Accounts payable are used for fixed asset acquisitions, the offset account for the fixed asset transaction is replaced by the vendor account that is selected for the transaction.</span></span>

<span data-ttu-id="51c5d-114">وبالنسبة لعمليات الاستحواذ التي تم ترحيلها باستخدام دفتر يومية المخزون إلى الأصول الثابتة في دفتر الأستاذ العام، فلا يتم شراء الأصل الثابت من مصادر خارجية، إلا أنه يتم تحويله من المخزون الخاص بالشركة.</span><span class="sxs-lookup"><span data-stu-id="51c5d-114">For acquisitions posted using the Inventory to fixed assets journal in General ledger, the fixed asset is not bought from external sources, but transferred from the company's own inventory.</span></span> <span data-ttu-id="51c5d-115">وبالتالي، يُعد حساب المقابل حساب إصدار مخزون لصنف المخزون بإدارة المخزون.</span><span class="sxs-lookup"><span data-stu-id="51c5d-115">Therefore, the offset account is an inventory issue account for the inventory item in Inventory management.</span></span>

<span data-ttu-id="51c5d-116">لمزيد من المعلومات، راجع [الحصول على الأصول عن طريق التدبير‬‏‫](acquire-assets-procurement.md).</span><span class="sxs-lookup"><span data-stu-id="51c5d-116">For more information, see [Acquire assets through procurement](acquire-assets-procurement.md).</span></span>



