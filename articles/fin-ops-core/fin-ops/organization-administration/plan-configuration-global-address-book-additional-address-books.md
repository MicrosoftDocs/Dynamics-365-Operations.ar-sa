---
title: التخطيط لإعداد دفتر العناوين العمومي ودفاتر العناوين الإضافية
description: تصف هذه المقالة الاعتبارات والقرارات التي يجب أن تتخذها خلال عملية التخطيط قبل إعداد وتكوين دفتر العناوين العمومي وأي دفاتر عناوين إضافية.
author: msftbrking
manager: AnnBe
ms.date: 01/13/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DirAddressBook, DirAddressBookTeam, DirParameters, DirPartyTable
audience: Application User
ms.reviewer: sericks
ms.custom: 23341
ms.assetid: a41cd8de-9ee0-4275-aea5-131db5326e5b
ms.search.region: Global
ms.author: brking
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8f0a53e1f9b378759e0c5adbe0612a5fa8cddc82
ms.sourcegitcommit: b112925c389a460a98c3401cc2c67df7091b066f
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 12/19/2020
ms.locfileid: "4796936"
---
# <a name="plan-for-the-global-address-book-and-other-address-books"></a><span data-ttu-id="2d6dc-103">التخطيط لدفتر عناوين عمومي ودفاتر العناوين الأخرى</span><span class="sxs-lookup"><span data-stu-id="2d6dc-103">Plan for the global address book and other address books</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2d6dc-104">تصف هذه المقالة الاعتبارات والقرارات التي يجب أن تتخذها خلال عملية التخطيط قبل إعداد وتكوين دفتر العناوين العمومي وأي دفاتر عناوين إضافية.</span><span class="sxs-lookup"><span data-stu-id="2d6dc-104">This topic describes the considerations and decisions that you must make during the planning process, before you set up and configure the global address book and any additional address books.</span></span> <span data-ttu-id="2d6dc-105">قد تتطلب منك بعض القرارات تأكيد القرارات التي تم اتخاذها لنواحٍ أخرى من المنتج، مثل التدرج الهرمي للمؤسسات.</span><span class="sxs-lookup"><span data-stu-id="2d6dc-105">Some of the decisions will require that you confirm the decisions that have been made for other areas of the product, such as the organization hierarchy.</span></span>

## <a name="global-address-book"></a><span data-ttu-id="2d6dc-106">دفتر العناوين العمومي</span><span class="sxs-lookup"><span data-stu-id="2d6dc-106">Global address book</span></span>

<span data-ttu-id="2d6dc-107">قبل البدء في العمل مع دفتر العناوين العمومي، يجب عليك تحديد القيم الافتراضية لذلك.</span><span class="sxs-lookup"><span data-stu-id="2d6dc-107">Before you begin to work with the global address book, you must determine the default values for it.</span></span> <span data-ttu-id="2d6dc-108">ويتم فيما بعد استخدام هذه القيم الافتراضية لأي دفاتر عناوين إضافية تقوم بإنشائها.</span><span class="sxs-lookup"><span data-stu-id="2d6dc-108">These default values are then used for any additional address books that you create.</span></span>

<span data-ttu-id="2d6dc-109">**القرارات**</span><span class="sxs-lookup"><span data-stu-id="2d6dc-109">**Decisions**</span></span>

- <span data-ttu-id="2d6dc-110">ما التسلسل الذي ينبغي به عرض الأسماء في سجلات الأطرف من نوع **الشخص**؟</span><span class="sxs-lookup"><span data-stu-id="2d6dc-110">What sequence should names be displayed in for party records of the **Person** type?</span></span> <span data-ttu-id="2d6dc-111">على سبيل المثال، يمثل تسلسل واحد الاسم الأخير، والاسم الأوسط، والاسم الأول.</span><span class="sxs-lookup"><span data-stu-id="2d6dc-111">For example, one sequence is last name, middle name, first name.</span></span>
- <span data-ttu-id="2d6dc-112">هل يجب حذف سجلات الأطراف من "دفتر العناوين" عند حذف سجل الدور؟</span><span class="sxs-lookup"><span data-stu-id="2d6dc-112">Should party records be deleted from the address book when the role record is deleted?</span></span> <span data-ttu-id="2d6dc-113">على سبيل المثال، إذا تم حذف سجل عميل، هل يجب حذف سجل الطرف أيضًا؟</span><span class="sxs-lookup"><span data-stu-id="2d6dc-113">For example, if a customer record is deleted, should the party record also be deleted?</span></span>
- <span data-ttu-id="2d6dc-114">عند إنشاء سجل جديد، هل يجب إعلام المستخدمين بما إذا تم العثور على سجل مكرر في دفتر العناوين العمومي؟</span><span class="sxs-lookup"><span data-stu-id="2d6dc-114">When a new record is created, should users be notified if a duplicate record is found in the global address book?</span></span>
- <span data-ttu-id="2d6dc-115">هل يجب تضمين رقم نظام الترقيم العالمي للبيانات (DUNS) في معلومات سجل الطرف؟</span><span class="sxs-lookup"><span data-stu-id="2d6dc-115">Should the Data Universal Numbering System (DUNS) number be included in a party record's information?</span></span>
- <span data-ttu-id="2d6dc-116">إذا تم تضمين رقم DUNS في سجل طرف، هل يجب فحص الطابع الفريد للرقم؟</span><span class="sxs-lookup"><span data-stu-id="2d6dc-116">If the DUNS number is included in a party record, should the uniqueness of the number be checked?</span></span>
- <span data-ttu-id="2d6dc-117">عندما يتم إنشاء سجل طرف في دفتر العناوين العمومي، هل تريد نوع الطرف الافتراضي أو الشخص أو المؤسسة؟</span><span class="sxs-lookup"><span data-stu-id="2d6dc-117">When a party record is created in the global address book, do you want a default party type, person, or organization?</span></span>
- <span data-ttu-id="2d6dc-118">ما أدوار المستخدم التي يجب أن يكون لديها وصول إلى العناوين الخاصة ومعلومات جهة اتصال سجلات الأطراف؟</span><span class="sxs-lookup"><span data-stu-id="2d6dc-118">Which user roles should have access to the private addresses and contact information of party records?</span></span>

## <a name="additional-address-books"></a><span data-ttu-id="2d6dc-119">دفاتر العناوين الإضافية</span><span class="sxs-lookup"><span data-stu-id="2d6dc-119">Additional address books</span></span>

<span data-ttu-id="2d6dc-120">بعد إنشاء "دفتر العناوين العمومي"، يمكنك إنشاء دفاتر عناوين إضافية عند اللزوم، مثل دفتر عناوين منفصلة لكل شركة في المؤسسة الخاصة بك أو لكل بند أعمال.</span><span class="sxs-lookup"><span data-stu-id="2d6dc-120">After you create the global address book, you can create additional address books as you require, such as a separate address book for each company in your organization or for each line of business.</span></span> <span data-ttu-id="2d6dc-121">على سبيل المثال، شركة الاتحاد للتصنيع هي مؤسسة دولية لها العديد من الشركات وبنود أعمال متعددة.</span><span class="sxs-lookup"><span data-stu-id="2d6dc-121">For example, Fabrikam is an international organization that has multiple companies and multiple lines of business.</span></span> <span data-ttu-id="2d6dc-122">وتخطط شركة الاتحاد للتصنيع لإنشاء دفتر عناوين لكل بند أعمال.</span><span class="sxs-lookup"><span data-stu-id="2d6dc-122">Fabrikam plans to create an address book for each line of business.</span></span> <span data-ttu-id="2d6dc-123">وبالنسبة لبنود الأعمال التي تحدث في موقع واحد أو أكثر، مثل أعمال الأدوات التي تعمل بالهواء المضغوط، تعتزم شركة الاتحاد للتصنيع إنشاء دفتر عناوين لكل موقع.</span><span class="sxs-lookup"><span data-stu-id="2d6dc-123">For lines of business that occur in more than one location, such as the pneumatic tools business, Fabrikam plans to create an address book for each location.</span></span> <span data-ttu-id="2d6dc-124">قام حمدي، وهو مدير تكنولوجيا المعلومات في شركة الاتحاد للتصنيع، بإنشاء القائمة التالية لدفاتر العناوين المطلوبة.</span><span class="sxs-lookup"><span data-stu-id="2d6dc-124">Chris, the IT manager at Fabrikam, has created the following list of address books that are required.</span></span> <span data-ttu-id="2d6dc-125">كما توضح هذه القائمة سجلات الأطراف التي يجب أن يشتمل عليها كل دفتر عناوين.</span><span class="sxs-lookup"><span data-stu-id="2d6dc-125">This list also describes the party records that each address book must include.</span></span>

- <span data-ttu-id="2d6dc-126">**عقود القطاع العام (PubSC)** – سجلات الأطراف لكافة الأطراف المشاركة في عقود القطاع العام التي تحتفظ بها شركة الاتحاد للتصنيع.</span><span class="sxs-lookup"><span data-stu-id="2d6dc-126">**Public Sector Contracts (PubSC)** – Party records for all parties that are involved in the public sector contracts that Fabrikam holds.</span></span>
- <span data-ttu-id="2d6dc-127">**عقود القطاع الخاص (PriSC)** – سجلات الأطراف لكافة الأطراف المشاركة في عقود القطاع الخاص التي تحتفظ بها شركة الاتحاد للتصنيع.</span><span class="sxs-lookup"><span data-stu-id="2d6dc-127">**Private Sector Contracts (PriSC)** – Party records for all parties that are involved in the private sector contracts that Fabrikam holds.</span></span>
- <span data-ttu-id="2d6dc-128">**الأدوات الإلكترونية (ET)** – سجلات الأطراف لكافة الأطراف التي تشارك في شراء أو بيع الأدوات الإلكترونية، أو التي تتفاعل مع الأدوات الإلكترونية التي توفرها أو شركة الاتحاد للتصنيع أو يتم شراؤها لها في شركة الاتحاد للتصنيع في شركة الاتحاد للتصنيع في اليابان.</span><span class="sxs-lookup"><span data-stu-id="2d6dc-128">**Electronic Tools (ET)** – Party records for all parties that are involved in the purchase or sale of electronic tools, or that otherwise interact with the electronic tools that are provided by or purchased for Fabrikam in the Fabrikam-Japan company.</span></span>
- <span data-ttu-id="2d6dc-129">**الأدوات التي تعمل بالهواء المضغوط (PTJPN)** – سجلات الأطراف لكافة الأطراف التي تشارك في شراء أو بيع الأدوات التي تعمل بالهواء الضغوط، أو التي تتفاعل مع الأدوات التي تعمل بالهواء المضغوط التي توفرها أو شركة الاتحاد للتصنيع أو يتم شراؤها لها في شركة الاتحاد للتصنيع في شركة الاتحاد للتصنيع في اليابان.</span><span class="sxs-lookup"><span data-stu-id="2d6dc-129">**Pneumatic Tools (PTJPN)** – Party records for all parties that are involved in the purchase or sale of pneumatic tools, or that otherwise interact with the pneumatic tools that are provided by or purchased for Fabrikam in the Fabrikam-Japan company.</span></span>
- <span data-ttu-id="2d6dc-130">**الأدوات التي تعمل بالهواء المضغوط (PTUSA)** – سجلات الأطراف لكافة الأطراف التي تشارك في شراء أو بيع الأدوات التي تعمل بالهواء الضغوط، أو التي تتفاعل مع الأدوات التي تعمل بالهواء المضغوط التي توفرها أو شركة الاتحاد للتصنيع أو يتم شراؤها لها في شركة الاتحاد للتصنيع في شركة الاتحاد للتصنيع في الولايات المتحدة.</span><span class="sxs-lookup"><span data-stu-id="2d6dc-130">**Pneumatic Tools (PTUSA)** – Party records for all parties that are involved in the purchase or sale of pneumatic tools, or that otherwise interact with the pneumatic tools that are provided by or purchased for Fabrikam in the Fabrikam-US company.</span></span>

<span data-ttu-id="2d6dc-131">**القرار:**</span><span class="sxs-lookup"><span data-stu-id="2d6dc-131">**Decision:**</span></span>

- <span data-ttu-id="2d6dc-132">كم عدد دفاتر عناوين الإضافية التي ستقوم بإنشائها؟</span><span class="sxs-lookup"><span data-stu-id="2d6dc-132">How many additional address books will you create?</span></span>
