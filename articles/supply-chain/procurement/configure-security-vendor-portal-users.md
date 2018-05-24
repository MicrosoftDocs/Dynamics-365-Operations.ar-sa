---
title: "أمان مستخدم مدخل المورّد على الإنترنت‬"
description: "تشرح هذه المقالة كيفية إعداد الأمان للمورّدين الخارجيين الذين يستخدمون مدخل المورّد. تنطبق هذه المعلومات فقط على إصدارات Dynamics AX لشهري فبراير 2016 ومايو 2016."
author: mkirknel
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SysUserManagement
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 30231
ms.assetid: 3574db17-81c7-4c5a-999b-0098aa0b9cda
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 5819d21a91ac2a7c91f19fd6d80fd7b983411545
ms.contentlocale: ar-sa
ms.lasthandoff: 05/08/2018

---

# <a name="vendor-portal-user-security"></a><span data-ttu-id="a1788-104">أمان مستخدم مدخل المورّد على الإنترنت‬</span><span class="sxs-lookup"><span data-stu-id="a1788-104">Vendor portal user security</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a1788-105">تشرح هذه المقالة كيفية إعداد الأمان للمورّدين الخارجيين الذين يستخدمون مدخل المورّد.</span><span class="sxs-lookup"><span data-stu-id="a1788-105">This article explains how to set up security for external vendors who use the Vendor portal.</span></span> <span data-ttu-id="a1788-106">تنطبق هذه المعلومات فقط على إصدارات Dynamics AX لشهري فبراير 2016 ومايو 2016.</span><span class="sxs-lookup"><span data-stu-id="a1788-106">This information applies only to the February 2016 &amp; May 2016 versions of Dynamics AX.</span></span>

<span data-ttu-id="a1788-107">‏‫تم استبدال وظيفة مدخل المورد بوظيفة تعاون المورد الموسعة في Dynamics 365 for Operations، الإصدار 1611.</span><span class="sxs-lookup"><span data-stu-id="a1788-107">The Vendor portal functionality has been replaced by extended vendor collaboration functionality in Dynamics 365 for Operations version 1611.</span></span> <span data-ttu-id="a1788-108">لمزيد من المعلومات حول إعداد الأمان لتعاون المورد، راجع [‬‏‫إعداد تعاون المورد والمحافظة عليه](set-up-maintain-vendor-collaboration.md).</span><span class="sxs-lookup"><span data-stu-id="a1788-108">For more information about setting up security for vendor collaboration, see [Set up and maintain vendor collaboration](set-up-maintain-vendor-collaboration.md).</span></span> <span data-ttu-id="a1788-109">يعرض مدخل الموردين مجموعة محدودة من المعلومات المتعلقة بأوامر الشراء (POs) للموردين الخارجيين.</span><span class="sxs-lookup"><span data-stu-id="a1788-109">The Vendor portal exposes a limited set of information about purchase orders (POs) to external vendors.</span></span> <span data-ttu-id="a1788-110">ومن المهم أن تقوم بشكل صحيح بإعداد أذونات المستخدم لمدخل الموردين في Microsoft Dynamics AX، حيث لا يصل الموردون بشكل غير مقصود إلى المعلومات الإضافية الموجودة في تثبيت Dynamics AX.</span><span class="sxs-lookup"><span data-stu-id="a1788-110">It's important that you correctly set up user permissions for the Vendor portal in Microsoft Dynamics AX, so that vendors don't have unintended access to additional information in your Dynamics AX installation.</span></span> <span data-ttu-id="a1788-111">**هام:** بخلاف المستخدمين الآخرين، يجب ألا يمتلك الموردون الخارجيون دور **SystemUser**.</span><span class="sxs-lookup"><span data-stu-id="a1788-111">**Important:** Unlike other users, external vendors should not have the **SystemUser** role.</span></span> <span data-ttu-id="a1788-112">يمنح دور **SystemUser** حق الوصول إلى مجموعة من الامتيازات غير المناسبة للمستخدمين الخارجيين.</span><span class="sxs-lookup"><span data-stu-id="a1788-112">The **SystemUser** role grants access to a set of privileges that aren't suitable for external users.</span></span>

## <a name="setting-up-a-vendor-portal-user"></a><span data-ttu-id="a1788-113">إعداد مستخدم مدخل الموردين</span><span class="sxs-lookup"><span data-stu-id="a1788-113">Setting up a Vendor portal user</span></span>
<span data-ttu-id="a1788-114">قبل إنشاء حساب مستخدم لشخص ما سيستخدم مدخل الموردين، يجب إعداد المورد للسماح بتعاون مدخل الموردين.</span><span class="sxs-lookup"><span data-stu-id="a1788-114">Before you create a user account for someone who will use the Vendor portal, you must set up the vendor to allow for Vendor portal collaboration.</span></span> <span data-ttu-id="a1788-115">واستخدم حقل **تعاون أمر الشراء** في علامة التبويب **عام** في صفحة **الموردين**.</span><span class="sxs-lookup"><span data-stu-id="a1788-115">Use the **Purchase order collaboration** field on the **General** tab on the **Vendors** page.</span></span> <span data-ttu-id="a1788-116">يجب على الموردين الخارجيين الذين يستخدمون مدخل الموردين القيام بالإعداد التالي:</span><span class="sxs-lookup"><span data-stu-id="a1788-116">External vendors that use the Vendor portal must have the following setup:</span></span>

-   <span data-ttu-id="a1788-117">يجب تسجيل حساب مستخدم Microsoft Azure Active Directory (AAD) للمورد في صفحة **المستخدمين** في Dynamics AX.</span><span class="sxs-lookup"><span data-stu-id="a1788-117">A Microsoft Azure Active Directory (AAD) user account must be registered for the vendor on the **Users** page in Dynamics AX.</span></span>
-   <span data-ttu-id="a1788-118">يجب أن يتوفر للمورد دور أمان **المورد (خارجي)**، وليس دور **SystemUser**.</span><span class="sxs-lookup"><span data-stu-id="a1788-118">The vendor must have the **Vendor (external)** security role, not the **SystemUser** role.</span></span> <span data-ttu-id="a1788-119">**ملاحظة:** يتم منح دور **SystemUser** تلقائياً عند إنشاء حساب مستخدم جديد في Dynamics AX.</span><span class="sxs-lookup"><span data-stu-id="a1788-119">**Note:** The **SystemUser** role is automatically granted when you create a new user account in Dynamics AX.</span></span> <span data-ttu-id="a1788-120">ولذلك، يجب إزالة هذا الدور والإقرار برسالة التحذير التي تتلقاها.</span><span class="sxs-lookup"><span data-stu-id="a1788-120">Therefore, you must remove that role and acknowledge the warning message that you receive.</span></span>
-   <span data-ttu-id="a1788-121">ويجب ألا يتم منح مستخدم المورد إذنًا لإضافة حقول إضافية من جداول أمر الشراء إلى طريقة عرض أمر الشراء.</span><span class="sxs-lookup"><span data-stu-id="a1788-121">The vendor user should not be granted permission to add additional fields from the PO tables to their view of the PO.</span></span> <span data-ttu-id="a1788-122">في علامة التبويب **تخصيص**، في علامة التبويب **المستخدمين**، قم بتعيين خيار **التخصيص الصريح المسوح به** للمستخدم إلى **لا**.</span><span class="sxs-lookup"><span data-stu-id="a1788-122">On the **Personalization** tab, on the **Users** tab, set the **Explicit personalization allowed** option for the user to **No**.</span></span>
-   <span data-ttu-id="a1788-123">يجب أن يكون حساب المستخدم مقترنًا بشخص جهة اتصال مسجلة.</span><span class="sxs-lookup"><span data-stu-id="a1788-123">The user account must be associated with a registered contact person.</span></span> <span data-ttu-id="a1788-124">وفي صفحة **المستخدمين**، حدد شخص جهة اتصال في حقل **الاسم**.</span><span class="sxs-lookup"><span data-stu-id="a1788-124">On the **Users** page, select a contact person in the **Name** field.</span></span> <span data-ttu-id="a1788-125">يجب أن يتوفر للشخص الذي قمت بتحديده دور **الاتصال** للمورد ذي الصلة.</span><span class="sxs-lookup"><span data-stu-id="a1788-125">The person that you select should have the **Contact** role for the relevant vendor.</span></span>

<span data-ttu-id="a1788-126">إذا كان نفس الشخص يتطلب الوصول إلى مدخل الموردين لعدة حسابات موردين (لمختلف الكيانات القانونية، على ما يُحتمل)، يجب إقران كل حساب من حسابات المستخدم الخاصة بهذا الشخص بنفس شخص جهة الاتصال المسجل.</span><span class="sxs-lookup"><span data-stu-id="a1788-126">If the same person requires access to the Vendor portal for multiple vendor accounts (for different legal entities, perhaps), each of that person's user accounts must be associated with the same registered contact person.</span></span> <span data-ttu-id="a1788-127">ويشتمل دور **المورد (خارجي)** على كافة القدرات الأساسية المطلوبة لاستخدام الوظيفة المتوفرة في مدخل المورد.</span><span class="sxs-lookup"><span data-stu-id="a1788-127">The **Vendor (external)** role includes all the basic capabilities that are required in order to use the functionality that is available in the Vendor portal.</span></span> <span data-ttu-id="a1788-128">يساعد هذا الإعداد على ضمان أن تكون واجهة المستخدم التي يشاهدها المستخدم الخارجي مركزةً على السيناريو المحدد فقط.</span><span class="sxs-lookup"><span data-stu-id="a1788-128">This setup helps guarantee that the user interface that the external user sees is focused on the intended scenario only.</span></span>

<a name="additional-resources"></a><span data-ttu-id="a1788-129">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="a1788-129">Additional resources</span></span>
--------

[<span data-ttu-id="a1788-130">تعاون المورد</span><span class="sxs-lookup"><span data-stu-id="a1788-130">Vendor collaboration</span></span>](collaborate-vendors-vendor-portal.md)




