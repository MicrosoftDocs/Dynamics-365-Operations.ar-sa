---
title: تثبيت مدخل العميل وإعداده وتحديثه
description: يوفر هذا الموضوع تفاصيل الترخيص وتعليمات حول إعداد مدخل العميل.
author: dasani-madipalli
manager: tfehr
ms.date: 04/22/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: damadipa
ms.search.validFrom: 2020-04-22
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: b9d1e742f78254d949dc49fda008d63b8bff4d65
ms.sourcegitcommit: 713b5dfc76a6875d0ba6d86c5cbd585ea502cf9d
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/01/2020
ms.locfileid: "3413930"
---
# <a name="install-set-up-and-update-the-customer-portal"></a><span data-ttu-id="ab3c5-103">تثبيت مدخل العميل وإعداده وتحديثه</span><span class="sxs-lookup"><span data-stu-id="ab3c5-103">Install, set up, and update the Customer portal</span></span>

## <a name="licensing-requirements"></a><span data-ttu-id="ab3c5-104">متطلبات الترخيص</span><span class="sxs-lookup"><span data-stu-id="ab3c5-104">Licensing requirements</span></span>

<span data-ttu-id="ab3c5-105">لتطبيق موقع العميل، يجب أن تتوفر لديك التراخيص التالية:</span><span class="sxs-lookup"><span data-stu-id="ab3c5-105">To implement the Customer portal, you must have the following licenses:</span></span>

- <span data-ttu-id="ab3c5-106">**مداخل Power Apps** – هذا الترخيص مطلوب لاستضافة مدخل العميل.</span><span class="sxs-lookup"><span data-stu-id="ab3c5-106">**Power Apps portals** – This license is required to host the Customer portal.</span></span> <span data-ttu-id="ab3c5-107">يتم ترخيص المداخل استنادًا إلى الاستخدام.</span><span class="sxs-lookup"><span data-stu-id="ab3c5-107">Portals are licensed based on usage.</span></span> <span data-ttu-id="ab3c5-108">لمزيد من المعلومات، راجع [متطلبات ترخيص مداخل Power Apps](https://docs.microsoft.com/power-platform/admin/powerapps-flow-licensing-faq#portals).</span><span class="sxs-lookup"><span data-stu-id="ab3c5-108">For more information, see the [Power Apps portals licensing requirements](https://docs.microsoft.com/power-platform/admin/powerapps-flow-licensing-faq#portals).</span></span>
- <span data-ttu-id="ab3c5-109">**الكتابة المزدوجة** - يجب أن تتوفر لديك التراخيص اللازمة لتمكين الكتابة المزدوجة لكيانات Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="ab3c5-109">**Dual-write** – You must have the necessary licenses to enable dual-write for Supply Chain Management entities.</span></span> <span data-ttu-id="ab3c5-110">لمزيد من المعلومات، راجع [متطلبات النظام للكتابة المزدوجة](../../fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-system-req.md).</span><span class="sxs-lookup"><span data-stu-id="ab3c5-110">For more information, see the [system requirements for dual-write](../../fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-system-req.md).</span></span>

## <a name="dependencies-on-dual-write-and-power-apps-portals"></a><span data-ttu-id="ab3c5-111">التبعيات على الكتابة المزدوجة ومداخل Power Apps</span><span class="sxs-lookup"><span data-stu-id="ab3c5-111">Dependencies on dual-write and Power Apps portals</span></span>

<span data-ttu-id="ab3c5-112">يعتمد مدخل العميل على مداخل Power Apps والكتابة المزدوجة، كما هو مبين في الشكل التوضيحي التالي.</span><span class="sxs-lookup"><span data-stu-id="ab3c5-112">The Customer portal depends on Power Apps portals and dual-write, as shown in the following illustration.</span></span>

![![تبعيات مدخل العميل](media/customer-portal-elements.png "تبعيات مدخل العميل")](media/customer-portal-elements.png "Customer portal dependencies")

<span data-ttu-id="ab3c5-114">بعكس الميزات الأخرى من Supply Chain Management، يقيم قالب مدخل العميل في مداخل Power Apps.</span><span class="sxs-lookup"><span data-stu-id="ab3c5-114">Unlike other features from Supply Chain Management, the Customer portal template resides in Power Apps portals.</span></span> <span data-ttu-id="ab3c5-115">وبالتالي، يتحدد مدخل العميل بالوظيفة والقدرات التي توفرها مداخل Power Apps في الكتابة المزدوجة.</span><span class="sxs-lookup"><span data-stu-id="ab3c5-115">Therefore, the Customer portal is limited by the functionality and capabilities that are provided by Power Apps portals and the entities in dual-write.</span></span>

## <a name="required-setup-to-enable-the-customer-portal"></a><a name="required-setup"></a><span data-ttu-id="ab3c5-116">الإعداد المطلوب لتمكين مدخل العميل</span><span class="sxs-lookup"><span data-stu-id="ab3c5-116">Required setup to enable the Customer portal</span></span>

<span data-ttu-id="ab3c5-117">بعد أن تتأكد من امتلاك التراخيص المطلوبة، يمكنك إعداد الكتابة المزدوجة كما ورد في [إرشادات المزامنة الأولية للكتابة المزدوجة](../../fin-ops-core/dev-itpro/data-entities/dual-write/initial-sync.md).</span><span class="sxs-lookup"><span data-stu-id="ab3c5-117">After you've made sure that you have the required licenses, you can set up dual-write as described in the [dual-write initial synchronization instructions](../../fin-ops-core/dev-itpro/data-entities/dual-write/initial-sync.md).</span></span>

<span data-ttu-id="ab3c5-118">تأكد من تمكين تعيينات الكيانات التالية في الكتابة المزدوجة:</span><span class="sxs-lookup"><span data-stu-id="ab3c5-118">Be sure to enable the following entity mappings in dual-write:</span></span>

- <span data-ttu-id="ab3c5-119">رأس أمر المبيعات</span><span class="sxs-lookup"><span data-stu-id="ab3c5-119">Sales Order Header</span></span>
- <span data-ttu-id="ab3c5-120">تفاصيل أمر المبيعات</span><span class="sxs-lookup"><span data-stu-id="ab3c5-120">Sales Order Details</span></span>
- <span data-ttu-id="ab3c5-121">الحسابات</span><span class="sxs-lookup"><span data-stu-id="ab3c5-121">Accounts</span></span>
- <span data-ttu-id="ab3c5-122">جهات الاتصال</span><span class="sxs-lookup"><span data-stu-id="ab3c5-122">Contacts</span></span>
- <span data-ttu-id="ab3c5-123">المنتجات</span><span class="sxs-lookup"><span data-stu-id="ab3c5-123">Products</span></span>

<span data-ttu-id="ab3c5-124">بعد اكتمال هذا الإعداد، يمكنك تزويد قالب مدخل العميل.</span><span class="sxs-lookup"><span data-stu-id="ab3c5-124">After this setup is completed, you can provision the Customer portal template.</span></span>

## <a name="provision-the-customer-portal"></a><span data-ttu-id="ab3c5-125">تزويد مدخل العميل</span><span class="sxs-lookup"><span data-stu-id="ab3c5-125">Provision the Customer portal</span></span>

<span data-ttu-id="ab3c5-126">قبل البدء، تأكد من إكمال [الإعداد المطلوب](#required-setup).</span><span class="sxs-lookup"><span data-stu-id="ab3c5-126">Before you begin, make sure that you've already completed the [required setup](#required-setup).</span></span> <span data-ttu-id="ab3c5-127">ثم اتبع الخطوات التالية لتزويد مدخل العميل.</span><span class="sxs-lookup"><span data-stu-id="ab3c5-127">Then follow these steps to provision the Customer portal.</span></span>

1. <span data-ttu-id="ab3c5-128">انتقل إلى [make.powerapps.com](https://make.powerapps.com/).</span><span class="sxs-lookup"><span data-stu-id="ab3c5-128">Go to [make.powerapps.com](https://make.powerapps.com/).</span></span>
2. <span data-ttu-id="ab3c5-129">تأكد من استخدام البيئة حيث قمت بتمكين الكتابة المزدوجة.</span><span class="sxs-lookup"><span data-stu-id="ab3c5-129">Make sure that you're using the environment where you enabled dual-write.</span></span>
3. <span data-ttu-id="ab3c5-130">من علامة التبويب **إنشاء**، قم بالتمرير لأسفل إلى القسم **بدء من القالب**، وحدد القالب المسمى **عميل Supply Chain Management**.</span><span class="sxs-lookup"><span data-stu-id="ab3c5-130">On the **Create** tab, scroll down to the **Start from template** section, and select the template that is named **Supply Chain Management Customer**.</span></span>
4. <span data-ttu-id="ab3c5-131">اتبع الإرشادات التي تظهر على الشاشة.</span><span class="sxs-lookup"><span data-stu-id="ab3c5-131">Follow the on-screen instructions.</span></span>

<span data-ttu-id="ab3c5-132">بعد اكتمال التزويد، يمكنك الوصول إلى مدخل العميل في قسم **تطبيقاتك** في **الصفحة الرئيسية**.</span><span class="sxs-lookup"><span data-stu-id="ab3c5-132">After provisioning is completed, you can access the Customer portal in the **Your apps** section of the **Home** page.</span></span>

> [!NOTE]
> <span data-ttu-id="ab3c5-133">إذا لم يكن حل الكتابة المزدوجة مثبتًا في البيئة التي تعمل فيها، فستتلقى رسالة خطأ، ولن يتم تزويد مدخل العميل.</span><span class="sxs-lookup"><span data-stu-id="ab3c5-133">If the dual-write solution isn't installed in the environment that you're working in, you will receive an error message, and the Customer portal won't be provisioned.</span></span>

## <a name="update-the-customer-portal"></a><span data-ttu-id="ab3c5-134">تحديث مدخل العميل</span><span class="sxs-lookup"><span data-stu-id="ab3c5-134">Update the Customer portal</span></span>

<span data-ttu-id="ab3c5-135">قد تُضاف وظائف إضافية إلى مدخل العميل لاحقًا.</span><span class="sxs-lookup"><span data-stu-id="ab3c5-135">More functionality might be added to the Customer portal later.</span></span> <span data-ttu-id="ab3c5-136">ستظهر تلقائيًا في بيئتك التغييرات التي تجريها Microsoft على مكون الحل الأساسية.</span><span class="sxs-lookup"><span data-stu-id="ab3c5-136">Any changes that Microsoft makes to the underlying solution components will automatically appear in your environment.</span></span> <span data-ttu-id="ab3c5-137">ومع ذلك، فإن موقع الويب الذي تم تزويده في بيئتك لن يعكس التغييرات التي يتم إدخالها على بيانات التكوين.</span><span class="sxs-lookup"><span data-stu-id="ab3c5-137">However, the website that is provisioned in your environment won't automatically reflect changes that are made to the configuration data.</span></span> <span data-ttu-id="ab3c5-138">سيتعين عليك تطبيق هذه التغييرات يدويًا عن طريق الحصول على التعليمات البرمجية من القالب الجديد ودمجه مع موقع ويب الذي تم تزويده.</span><span class="sxs-lookup"><span data-stu-id="ab3c5-138">You will have to manually apply those changes by getting the code from the new template and merging it with the provisioned website.</span></span>

## <a name="resources"></a><span data-ttu-id="ab3c5-139">الموارد</span><span class="sxs-lookup"><span data-stu-id="ab3c5-139">Resources</span></span>

<span data-ttu-id="ab3c5-140">لمعرفة كيفية إعداد مدخل العميل وتخصيصه، يجب البدء بمراجعة الوثائق التالية للتقنيات الأساسية:</span><span class="sxs-lookup"><span data-stu-id="ab3c5-140">To learn how you can set up and customize the Customer portal, you should start by reviewing the following documentation for the underlying technologies:</span></span>

- [<span data-ttu-id="ab3c5-141">وثائق مداخل Power Apps</span><span class="sxs-lookup"><span data-stu-id="ab3c5-141">Power Apps portals documentation</span></span>](https://docs.microsoft.com/powerapps/maker/portals/overview)
- [<span data-ttu-id="ab3c5-142">وثائق الكتابة المزدوجة</span><span class="sxs-lookup"><span data-stu-id="ab3c5-142">Dual-write documentation</span></span>](../../fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-home-page.md)

<span data-ttu-id="ab3c5-143">لإدارة المداخل بطريقة فعالة، يجب فهم مداخل Power Apps ودورة حياة Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="ab3c5-143">To effectively manage your portals, you must understand the Power Apps portals and Common Data Service lifecycle.</span></span> <span data-ttu-id="ab3c5-144">لمزيد من المعلومات، راجع الموارد التالية:</span><span class="sxs-lookup"><span data-stu-id="ab3c5-144">For more information, see the following resources:</span></span>

- [<span data-ttu-id="ab3c5-145">حول دورة حياة المدخل</span><span class="sxs-lookup"><span data-stu-id="ab3c5-145">About portal lifecycle</span></span>](https://docs.microsoft.com/powerapps/maker/portals/admin/portal-lifecycle)
- [<span data-ttu-id="ab3c5-146">ترقية مدخل</span><span class="sxs-lookup"><span data-stu-id="ab3c5-146">Upgrade a portal</span></span>](https://docs.microsoft.com/powerapps/maker/portals/admin/upgrade-portal)
- [<span data-ttu-id="ab3c5-147">ترحيل تكوين المدخل</span><span class="sxs-lookup"><span data-stu-id="ab3c5-147">Migrate portal configuration</span></span>](https://docs.microsoft.com/powerapps/maker/portals/admin/migrate-portal-configuration)
- [<span data-ttu-id="ab3c5-148">إدارة دورة حياة الحل: تطبيقات Dynamics 365 for Customer Engagement</span><span class="sxs-lookup"><span data-stu-id="ab3c5-148">Solution Lifecycle Management: Dynamics 365 for Customer Engagement apps</span></span>](https://www.microsoft.com/download/details.aspx?id=57777)
