---
title: الترحيل باستخدام الدفاتر المشتقة
description: توضح هذه المقالة كيفية استخدام الدفاتر المشتقة.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetBookTable, LedgerJournalTransAsset
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 3421
ms.assetid: f5187c21-eec5-4148-b178-b8a5feff7f23
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2b58b2da949211f7eef804af98c866bf5074d47f
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/27/2019
ms.locfileid: "2187120"
---
# <a name="post-with-derived-books"></a><span data-ttu-id="e1207-103">الترحيل باستخدام الدفاتر المشتقة</span><span class="sxs-lookup"><span data-stu-id="e1207-103">Post with derived books</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e1207-104">توضح هذه المقالة كيفية استخدام الدفاتر المشتقة.</span><span class="sxs-lookup"><span data-stu-id="e1207-104">This article describes how to use derived books.</span></span>

<span data-ttu-id="e1207-105">عندما تقوم بترحيل الحركات لدفتر يحتوي على دفاتر مشتقة، يتم ترحيل حركات الدفاتر المشتقة تلقائيًا في دفاتر اليومية أو أوامر الشراء أو فواتير النص الحر.</span><span class="sxs-lookup"><span data-stu-id="e1207-105">When you post transactions for a book that contains derived books, the derived book transactions are posted automatically in journals, purchase orders, or free text invoices.</span></span> <span data-ttu-id="e1207-106">ومع ذلك، إذا قمت بإعداد حركات الدفاتر الأساسية في دفتر يومية الأصول الثابتة، فيمكنك عرض مبالغ الحركات المشتقة وتعديلها قبل ترحيلها.</span><span class="sxs-lookup"><span data-stu-id="e1207-106">However, if you prepare the primary book transactions in the Fixed assets journal, you can view and modify the amounts of the derived transactions before you post them.</span></span>
-   <span data-ttu-id="e1207-107">يتم تحديث حسابات معينة، مثل ضريبة المبيعات وحسابات العميل أو المورد مرة واحدة فقط عن طريق ترحيلات الدفتر الأساسي.</span><span class="sxs-lookup"><span data-stu-id="e1207-107">Certain accounts, such as sales tax and customer or vendor accounts, are updated only once by postings of the primary book.</span></span> <span data-ttu-id="e1207-108">ويتم ترحيل حركات الدفاتر المشتقة إلى الحسابات التي تم تحديدها للدفتر المشتق في صفحة ملفات تعريف ترحيل الأصول الثابتة.‬</span><span class="sxs-lookup"><span data-stu-id="e1207-108">The derived book transactions are posted to the accounts that have been defined for the derived book in the Fixed asset posting profiles page.</span></span>
-   <span data-ttu-id="e1207-109">يتم استخدام الاستحواذ في أغلب الأحيان كنوع الحركة للدفاتر المشتقة.</span><span class="sxs-lookup"><span data-stu-id="e1207-109">Acquisition is often used as the transaction type for the derived books.</span></span> <span data-ttu-id="e1207-110">سوف تستخدم هذا عند لزوم تطبيق الدفتر والدفتر المشتق على الأصول الثابتة من وقت الاستحواذ على الأصل الثابت.</span><span class="sxs-lookup"><span data-stu-id="e1207-110">You use this when the book and the derived book should be applied to the fixed asset from the time of the acquisition of the fixed asset.</span></span>
-   <span data-ttu-id="e1207-111">كما يُمكن أيضًا تطبيق قيم أخرى لنوع الحركة.</span><span class="sxs-lookup"><span data-stu-id="e1207-111">Other values for the transaction type can also apply.</span></span> <span data-ttu-id="e1207-112">على سبيل المثال، إذا كان الدفتر الأساسي والدفاتر المشتقة لهما الفترات الزمنية نفسها فيما يتعلق بعمليات البيع أو التخلص، فستتوفر كافة أنواع حركات الأصول الثابتة لإعداد دفتر مشتق.</span><span class="sxs-lookup"><span data-stu-id="e1207-112">For example, if the primary book and the derived books have the same intervals regarding sale or disposal, all fixed asset transaction types are available for the setup of a derived book.</span></span>

> [!WARNING]
> <span data-ttu-id="e1207-113">سيكون مبلغ الإهلاك الذي تم ترحيله في الدفتر المشتق هو نفسه المبلغ الذي تم ترحيله للدفتر الأساسي.</span><span class="sxs-lookup"><span data-stu-id="e1207-113">Depreciation posted in the derived book will be the same amount as was posted for the primary book.</span></span> <span data-ttu-id="e1207-114">وإذا كانت طرق الإهلاك مختلفة بين الدفاتر، فلا يجب إنشاء حركات إهلاك باستخدام العملية المشتقة.</span><span class="sxs-lookup"><span data-stu-id="e1207-114">If the depreciation methods are different between the books, you should not generate depreciation transactions using the derived process.</span></span> |

## <a name="example"></a><span data-ttu-id="e1207-115">مثال</span><span class="sxs-lookup"><span data-stu-id="e1207-115">Example</span></span> 
<span data-ttu-id="e1207-116">توضح المعلومات التالية كيفية إعداد حركات الاستحواذ باستخدام وظيفة الدفتر المشتق.</span><span class="sxs-lookup"><span data-stu-id="e1207-116">The following information describes how to set up acquisition transactions with the derived book functionality.</span></span>

1.  <span data-ttu-id="e1207-117">إنشاء الدفاتر في صفحة الدفاتر.</span><span class="sxs-lookup"><span data-stu-id="e1207-117">Create the books on the Books page.</span></span>
    -   <span data-ttu-id="e1207-118">دفتر المحاسبة: VM 1، طبقة الترحيل الحالية</span><span class="sxs-lookup"><span data-stu-id="e1207-118">The book for accounting: VM 1, Current posting layer</span></span>
    -   <span data-ttu-id="e1207-119">الدفتر للأغراض الضريبية‬: VM 2، طبقة ترحيل الضريبة</span><span class="sxs-lookup"><span data-stu-id="e1207-119">The book for tax purposes: VM 2, Tax posting layer</span></span>

2.  <span data-ttu-id="e1207-120">في نموذج القيمة VM 1، انقر فوق علامة تبويب "الدفاتر المشتقة". حدد نموذج القيمة VM 2 في حقل "الدفتر‬"، وحدد "الاستحواذ‬" في حقل "نوع الحركة".</span><span class="sxs-lookup"><span data-stu-id="e1207-120">On VM 1, click the Derived books tab. Select VM 2 in the Book field, and Acquisition in the Transaction type field.</span></span>

<span data-ttu-id="e1207-121">يمكن عندئذٍ إرفاق الدفاتر بأصول ثابتة معينة.</span><span class="sxs-lookup"><span data-stu-id="e1207-121">The books then can be attached to specific fixed assets.</span></span> 

<span data-ttu-id="e1207-122">عند ترحيل امتلاك لأصل ثابت بالدفتر VM 1، لا يتم ترحيل الامتلاك في VM 1 فقط، ولكن يتم ترحيله أيضًا في الدفتر المشتق VM 2.</span><span class="sxs-lookup"><span data-stu-id="e1207-122">When an acquisition is posted for a fixed asset with book VM 1, the acquisition is posted not only on VM 1, but also on the derived book VM 2.</span></span> <span data-ttu-id="e1207-123">ويتم تحديث حالة دفتري قيم الأصول الثابتة إلى "فتح".‬</span><span class="sxs-lookup"><span data-stu-id="e1207-123">The status of both fixed asset books is updated to Open.</span></span>

> [!NOTE]                                                                                                         
> <span data-ttu-id="e1207-124">إذا لم تستخدم الدفاتر المشتقة، فيجب عليك ترحيل الاستحواذ على الأصل الثابت لكل من الدفتر VM 1 والدفتر VM 2.</span><span class="sxs-lookup"><span data-stu-id="e1207-124">If you do not use derived books, you must post the acquisition of the fixed asset both for book VM 1 and book VM 2.</span></span>

<span data-ttu-id="e1207-125">لمزيد من المعلومات، راجع [‏‫الدفاتر المشتقة](derived-books.md).</span><span class="sxs-lookup"><span data-stu-id="e1207-125">For more information, see [Derived books](derived-books.md)</span></span>


