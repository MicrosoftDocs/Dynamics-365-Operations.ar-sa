---
title: "التخطيط لتكوين دفتر العناوين العمومي ودفاتر العناوين الإضافية"
description: "يوضح هذا الموضوع الاعتبارات والقرارات التي يجب أن تتخذها خلال عملية التخطيط قبل إعداد وتكوين دفتر العناوين العمومي وأي دفاتر عناوين إضافية في Microsoft Dynamics 365 for Finance and Operations. قد تتطلب منك بعض القرارات تأكيد القرارات التي تم اتخاذها لنواحٍ أخرى من المنتج، مثل التدرج الهرمي للمؤسسات."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 11/03/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: DirAddressBook, DirAddressBookTeam, DirParameters, DirPartyTable
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 23341
ms.assetid: a41cd8de-9ee0-4275-aea5-131db5326e5b
ms.search.region: Global
ms.author: shiva.pandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: b872603f987b72faacc0a987aa44c31e773636f8
ms.contentlocale: ar-sa
ms.lasthandoff: 11/03/2017

---

# <a name="plan-how-to-configure-the-global-address-book-and-additional-address-books"></a><span data-ttu-id="2e63c-104">التخطيط لتكوين دفتر العناوين العمومي ودفاتر العناوين الإضافية</span><span class="sxs-lookup"><span data-stu-id="2e63c-104">Plan how to configure the global address book and additional address books</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="2e63c-105">يوضح هذا الموضوع الاعتبارات والقرارات التي يجب أن تتخذها خلال عملية التخطيط قبل إعداد وتكوين دفتر العناوين العمومي وأي دفاتر عناوين إضافية في Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="2e63c-105">This topic describes the considerations and decisions that you must make during the planning process, before you set up and configure the global address book and any additional address books in Microsoft Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="2e63c-106">قد تتطلب منك بعض القرارات تأكيد القرارات التي تم اتخاذها لنواحٍ أخرى من المنتج، مثل التدرج الهرمي للمؤسسات.</span><span class="sxs-lookup"><span data-stu-id="2e63c-106">Some of the decisions will require that you confirm the decisions that have been made for other areas of the product, such as the organization hierarchy.</span></span>

<a name="global-address-book"></a><span data-ttu-id="2e63c-107">دفتر العناوين العمومي</span><span class="sxs-lookup"><span data-stu-id="2e63c-107">Global address book</span></span>
-------------------

<span data-ttu-id="2e63c-108">قبل البدء في العمل مع دفتر العناوين العمومي، يجب عليك تحديد القيم الافتراضية لذلك.</span><span class="sxs-lookup"><span data-stu-id="2e63c-108">Before you begin to work with the global address book, you must determine the default values for it.</span></span> <span data-ttu-id="2e63c-109">ويتم فيما بعد استخدام هذه القيم الافتراضية لأي دفاتر عناوين إضافية تقوم بإنشائها.</span><span class="sxs-lookup"><span data-stu-id="2e63c-109">These default values are then used for any additional address books that you create.</span></span> 

<span data-ttu-id="2e63c-110">**القرارات:**</span><span class="sxs-lookup"><span data-stu-id="2e63c-110">**Decisions:**</span></span>

-   <span data-ttu-id="2e63c-111">ما التسلسل الذي ينبغي به عرض الأسماء في سجلات الأطرف من نوع **الشخص**؟</span><span class="sxs-lookup"><span data-stu-id="2e63c-111">What sequence should names be displayed in for party records of the **Person** type?</span></span> <span data-ttu-id="2e63c-112">على سبيل المثال، يمثل تسلسل واحد الاسم الأخير، والاسم الأوسط، والاسم الأول.</span><span class="sxs-lookup"><span data-stu-id="2e63c-112">For example, one sequence is last name, middle name, first name.</span></span>
-   <span data-ttu-id="2e63c-113">هل يجب حذف سجلات الأطراف من "دفتر العناوين" عند حذف سجل الدور؟</span><span class="sxs-lookup"><span data-stu-id="2e63c-113">Should party records be deleted from the address book when the role record is deleted?</span></span> <span data-ttu-id="2e63c-114">على سبيل المثال، إذا تم حذف سجل عميل، هل يجب حذف سجل الطرف أيضًا؟</span><span class="sxs-lookup"><span data-stu-id="2e63c-114">For example, if a customer record is deleted, should the party record also be deleted?</span></span>
-   <span data-ttu-id="2e63c-115">عند إنشاء سجل جديد، هل يجب إعلام المستخدمين بما إذا تم العثور على سجل مكرر في دفتر العناوين العمومي؟</span><span class="sxs-lookup"><span data-stu-id="2e63c-115">When a new record is created, should users be notified if a duplicate record is found in the global address book?</span></span>
-   <span data-ttu-id="2e63c-116">هل يجب تضمين رقم نظام الترقيم العالمي للبيانات (DUNS) في معلومات سجل الطرف؟</span><span class="sxs-lookup"><span data-stu-id="2e63c-116">Should the Data Universal Numbering System (DUNS) number be included in a party record’s information?</span></span>
-   <span data-ttu-id="2e63c-117">إذا تم تضمين رقم DUNS في سجل طرف، هل يجب فحص الطابع الفريد للرقم؟</span><span class="sxs-lookup"><span data-stu-id="2e63c-117">If the DUNS number is included in a party record, should the uniqueness of the number be checked?</span></span>
-   <span data-ttu-id="2e63c-118">عندما يتم إنشاء سجل طرف في دفتر العناوين العمومي، هل تريد نوع الطرف الافتراضي أو الشخص أو المؤسسة؟</span><span class="sxs-lookup"><span data-stu-id="2e63c-118">When a party record is created in the global address book, do you want a default party type, person, or organization?</span></span>
-   <span data-ttu-id="2e63c-119">ما أدوار المستخدم التي يجب أن يكون لديها وصول إلى العناوين الخاصة ومعلومات جهة اتصال سجلات الأطراف؟</span><span class="sxs-lookup"><span data-stu-id="2e63c-119">Which user roles should have access to the private addresses and contact information of party records?</span></span>

## <a name="additional-address-books"></a><span data-ttu-id="2e63c-120">دفاتر العناوين الإضافية</span><span class="sxs-lookup"><span data-stu-id="2e63c-120">Additional address books</span></span>
<span data-ttu-id="2e63c-121">بعد إنشاء "دفتر العناوين العمومي"، يمكنك إنشاء دفاتر عناوين إضافية عند اللزوم، مثل دفتر عناوين منفصلة لكل شركة في المؤسسة الخاصة بك أو لكل بند أعمال.</span><span class="sxs-lookup"><span data-stu-id="2e63c-121">After you create the global address book, you can create additional address books as you require, such as a separate address book for each company in your organization or for each line of business.</span></span> <span data-ttu-id="2e63c-122">على سبيل المثال، شركة الاتحاد للتصنيع هي مؤسسة دولية لها العديد من الشركات وبنود أعمال متعددة.</span><span class="sxs-lookup"><span data-stu-id="2e63c-122">For example, Fabrikam is an international organization that has multiple companies and multiple lines of business.</span></span> <span data-ttu-id="2e63c-123">وتخطط شركة الاتحاد للتصنيع لإنشاء دفتر عناوين لكل بند أعمال.</span><span class="sxs-lookup"><span data-stu-id="2e63c-123">Fabrikam plans to create an address book for each line of business.</span></span> <span data-ttu-id="2e63c-124">وبالنسبة لبنود الأعمال التي تحدث في موقع واحد أو أكثر، مثل أعمال الأدوات التي تعمل بالهواء المضغوط، تعتزم شركة الاتحاد للتصنيع إنشاء دفتر عناوين لكل موقع.</span><span class="sxs-lookup"><span data-stu-id="2e63c-124">For lines of business that occur in more than one location, such as the pneumatic tools business, Fabrikam plans to create an address book for each location.</span></span> <span data-ttu-id="2e63c-125">قام حمدي، وهو مدير تكنولوجيا المعلومات في شركة الاتحاد للتصنيع، بإنشاء القائمة التالية لدفاتر العناوين المطلوبة.</span><span class="sxs-lookup"><span data-stu-id="2e63c-125">Chris, the IT manager at Fabrikam, has created the following list of address books that are required.</span></span> <span data-ttu-id="2e63c-126">كما توضح هذه القائمة سجلات الأطراف التي يجب أن يشتمل عليها كل دفتر عناوين.</span><span class="sxs-lookup"><span data-stu-id="2e63c-126">This list also describes the party records that each address book must include.</span></span>

-   <span data-ttu-id="2e63c-127">**عقود القطاع العام (PubSC)** – سجلات الأطراف لكافة الأطراف المشاركة في عقود القطاع العام التي تحتفظ بها شركة الاتحاد للتصنيع.</span><span class="sxs-lookup"><span data-stu-id="2e63c-127">**Public Sector Contracts (PubSC)** – Party records for all parties that are involved in the public sector contracts that Fabrikam holds.</span></span>
-   <span data-ttu-id="2e63c-128">**عقود القطاع الخاص (PriSC)** – سجلات الأطراف لكافة الأطراف المشاركة في عقود القطاع الخاص التي تحتفظ بها شركة الاتحاد للتصنيع.</span><span class="sxs-lookup"><span data-stu-id="2e63c-128">**Private Sector Contracts (PriSC)** – Party records for all parties that are involved in the private sector contracts that Fabrikam holds.</span></span>
-   <span data-ttu-id="2e63c-129">**الأدوات الإلكترونية (ET)** – سجلات الأطراف لكافة الأطراف التي تشارك في شراء أو بيع الأدوات الإلكترونية، أو التي تتفاعل مع الأدوات الإلكترونية التي توفرها أو شركة الاتحاد للتصنيع أو يتم شراؤها لها في شركة الاتحاد للتصنيع في شركة الاتحاد للتصنيع في اليابان.</span><span class="sxs-lookup"><span data-stu-id="2e63c-129">**Electronic Tools (ET)** – Party records for all parties that are involved in the purchase or sale of electronic tools, or that otherwise interact with the electronic tools that are provided by or purchased for Fabrikam in the Fabrikam-Japan company.</span></span>
-   <span data-ttu-id="2e63c-130">**الأدوات التي تعمل بالهواء المضغوط (PTJPN)** – سجلات الأطراف لكافة الأطراف التي تشارك في شراء أو بيع الأدوات التي تعمل بالهواء الضغوط، أو التي تتفاعل مع الأدوات التي تعمل بالهواء المضغوط التي توفرها أو شركة الاتحاد للتصنيع أو يتم شراؤها لها في شركة الاتحاد للتصنيع في شركة الاتحاد للتصنيع في اليابان.</span><span class="sxs-lookup"><span data-stu-id="2e63c-130">**Pneumatic Tools (PTJPN)** – Party records for all parties that are involved in the purchase or sale of pneumatic tools, or that otherwise interact with the pneumatic tools that are provided by or purchased for Fabrikam in the Fabrikam-Japan company.</span></span>
-   <span data-ttu-id="2e63c-131">**الأدوات التي تعمل بالهواء المضغوط (PTUSA)** – سجلات الأطراف لكافة الأطراف التي تشارك في شراء أو بيع الأدوات التي تعمل بالهواء الضغوط، أو التي تتفاعل مع الأدوات التي تعمل بالهواء المضغوط التي توفرها أو شركة الاتحاد للتصنيع أو يتم شراؤها لها في شركة الاتحاد للتصنيع في شركة الاتحاد للتصنيع في الولايات المتحدة.</span><span class="sxs-lookup"><span data-stu-id="2e63c-131">**Pneumatic Tools (PTUSA)** – Party records for all parties that are involved in the purchase or sale of pneumatic tools, or that otherwise interact with the pneumatic tools that are provided by or purchased for Fabrikam in the Fabrikam-US company.</span></span>

<span data-ttu-id="2e63c-132">**القرار:**</span><span class="sxs-lookup"><span data-stu-id="2e63c-132">**Decision:**</span></span>

-   <span data-ttu-id="2e63c-133">كم عدد دفاتر عناوين الإضافية التي ستقوم بإنشائها؟</span><span class="sxs-lookup"><span data-stu-id="2e63c-133">How many additional address books will you create?</span></span>

### <a name="address-book-security"></a><span data-ttu-id="2e63c-134">أمان دفتر العناوين</span><span class="sxs-lookup"><span data-stu-id="2e63c-134">Address book security</span></span>

<span data-ttu-id="2e63c-135">يمكن إنشاء دفاتر العناوين في أي وقت، ويمكنك أيضًا تعيين معلمات الأمان لدفاتر العناوين في أي وقت.</span><span class="sxs-lookup"><span data-stu-id="2e63c-135">You can create address books at any time, and you can also set security parameters for the address books at any time.</span></span> <span data-ttu-id="2e63c-136">ولا تحتاج لتعيين امتيازات الأمان لدفتر عناوين، ولكن إذا لم تقم بذلك، يمكن لجميع العمال في المؤسسة عرض كافة سجلات الأطراف في دفتر العناوين هذا.</span><span class="sxs-lookup"><span data-stu-id="2e63c-136">You aren't required to set security privileges for an address book, but if you don't, all workers in your organization can view all party records in that address book.</span></span> <span data-ttu-id="2e63c-137">ويمكنك تعيين امتيازات الأمان إلى سجلات الأطراف من خلال دفاتر العناوين.</span><span class="sxs-lookup"><span data-stu-id="2e63c-137">You can set security privileges to party records through address books.</span></span> <span data-ttu-id="2e63c-138">امتيازات الأمان استناداً إلى فرق العمل.</span><span class="sxs-lookup"><span data-stu-id="2e63c-138">Security privileges are based on teams.</span></span> <span data-ttu-id="2e63c-139">يضمن هذا النهج أن العمال وحدهم الذين يتم تعيينهم لفريق لديهم حق الوصول إلى دفتر عناوين يمكنهم عرض سجلات الأطراف في دفتر العناوين هذا.</span><span class="sxs-lookup"><span data-stu-id="2e63c-139">This approach guarantees that only workers who are assigned to a team that has access to an address book can view the party records in that address book.</span></span> <span data-ttu-id="2e63c-140">ويجب عليك تحديد الفرق التي لديها حق الوصول إلى كل دفتر عناوين.</span><span class="sxs-lookup"><span data-stu-id="2e63c-140">You must select the teams that have access to each address book.</span></span> <span data-ttu-id="2e63c-141">وفي كل دفتر عناوين، يمكنك تعيين امتيازات الأمان التي تتيح أو ترفض الوصول إلى فرق محددة.</span><span class="sxs-lookup"><span data-stu-id="2e63c-141">For each address book, you can set security privileges that allow or deny access to specific teams.</span></span> <span data-ttu-id="2e63c-142">وإذا قمت بمنح امتيازات فريق إلى دفتر عناوين، فإنه يمكن لجميع أعضاء الفريق عرض السجلات في دفتر العناوين هذا.</span><span class="sxs-lookup"><span data-stu-id="2e63c-142">If you grant a team privileges to an address book, all members of that team can view the records in the address book.</span></span> <span data-ttu-id="2e63c-143">وإذا لم تمنح وصول فريق إلى دفتر عناوين، فإنه لا يمكن لجميع أعضاء الفريق عرض دفتر العناوين أو محتوياته.</span><span class="sxs-lookup"><span data-stu-id="2e63c-143">If you don't grant a team access to an address book, the members of that team can't view the address book or its contents.</span></span> 

<span data-ttu-id="2e63c-144">**القرار:**</span><span class="sxs-lookup"><span data-stu-id="2e63c-144">**Decision:**</span></span>

-   <span data-ttu-id="2e63c-145">ما فرق العمل التي ينبغي أن يُتاح لها الوصول إلى كل دفتر عناوين جديد ستقوم بإنشائه؟</span><span class="sxs-lookup"><span data-stu-id="2e63c-145">Which teams should have access to each new address book that you will create?</span></span>





