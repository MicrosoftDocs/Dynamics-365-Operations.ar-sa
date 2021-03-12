---
title: تثبيت مدخل العميل وإعداده وتحديثه
description: يوفر هذا الموضوع تفاصيل الترخيص وتعليمات حول إعداد مدخل العميل.
author: dasani-madipalli
manager: tfehr
ms.date: 06/08/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: damadipa
ms.search.validFrom: 2020-04-22
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: 2153bbca2be7c72e48b9dc51b1f7fdbe2ab89903
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/15/2021
ms.locfileid: "4977728"
---
# <a name="install-set-up-and-update-the-customer-portal"></a><span data-ttu-id="62413-103">تثبيت مدخل العميل وإعداده وتحديثه</span><span class="sxs-lookup"><span data-stu-id="62413-103">Install, set up, and update the Customer portal</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

## <a name="licensing-requirements"></a><span data-ttu-id="62413-104">متطلبات الترخيص</span><span class="sxs-lookup"><span data-stu-id="62413-104">Licensing requirements</span></span>

<span data-ttu-id="62413-105">لتطبيق موقع العميل، يجب أن تتوفر لديك التراخيص التالية:</span><span class="sxs-lookup"><span data-stu-id="62413-105">To implement the Customer portal, you must have the following licenses:</span></span>

- <span data-ttu-id="62413-106">**مداخل Power Apps** – هذا الترخيص مطلوب لاستضافة مدخل العميل.</span><span class="sxs-lookup"><span data-stu-id="62413-106">**Power Apps portals** – This license is required to host the Customer portal.</span></span> <span data-ttu-id="62413-107">يتم ترخيص المداخل استنادًا إلى الاستخدام.</span><span class="sxs-lookup"><span data-stu-id="62413-107">Portals are licensed based on usage.</span></span> <span data-ttu-id="62413-108">لمزيد من المعلومات، راجع [متطلبات ترخيص مداخل Power Apps](https://docs.microsoft.com/power-platform/admin/powerapps-flow-licensing-faq#portals).</span><span class="sxs-lookup"><span data-stu-id="62413-108">For more information, see the [Power Apps portals licensing requirements](https://docs.microsoft.com/power-platform/admin/powerapps-flow-licensing-faq#portals).</span></span>
- <span data-ttu-id="62413-109">**الكتابة المزدوجة** - يجب أن تتوفر لديك التراخيص اللازمة لتمكين الكتابة المزدوجة لجداول Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="62413-109">**Dual-write** – You must have the necessary licenses to enable dual-write for Supply Chain Management tables.</span></span> <span data-ttu-id="62413-110">لمزيد من المعلومات، راجع [متطلبات النظام للكتابة المزدوجة](../../fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-system-req.md).</span><span class="sxs-lookup"><span data-stu-id="62413-110">For more information, see the [system requirements for dual-write](../../fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-system-req.md).</span></span>

## <a name="dependencies-on-dual-write-and-power-apps-portals"></a><span data-ttu-id="62413-111">التبعيات على الكتابة المزدوجة ومداخل Power Apps</span><span class="sxs-lookup"><span data-stu-id="62413-111">Dependencies on dual-write and Power Apps portals</span></span>

<span data-ttu-id="62413-112">يعتمد مدخل العميل على مداخل Power Apps والكتابة المزدوجة، كما هو مبين في الشكل التوضيحي التالي.</span><span class="sxs-lookup"><span data-stu-id="62413-112">The Customer portal depends on Power Apps portals and dual-write, as shown in the following illustration.</span></span>

<span data-ttu-id="62413-113">![تبعيات مدخل العميل](media/customer-portal-elements.png "تبعيات مدخل العميل")</span><span class="sxs-lookup"><span data-stu-id="62413-113">![Customer portal dependencies](media/customer-portal-elements.png "Customer portal dependencies")</span></span>

<span data-ttu-id="62413-114">بعكس الميزات الأخرى من Supply Chain Management، يقيم قالب مدخل العميل في مداخل Power Apps.</span><span class="sxs-lookup"><span data-stu-id="62413-114">Unlike other features from Supply Chain Management, the Customer portal template resides in Power Apps portals.</span></span> <span data-ttu-id="62413-115">وبالتالي، يتحدد مدخل العميل بالوظيفة والقدرات التي توفرها مداخل وجداول Power Apps في الكتابة المزدوجة.</span><span class="sxs-lookup"><span data-stu-id="62413-115">Therefore, the Customer portal is limited by the functionality and capabilities that are provided by Power Apps portals and the tables in dual-write.</span></span>

## <a name="required-setup-to-enable-the-customer-portal"></a><a name="required-setup"></a><span data-ttu-id="62413-116">الإعداد المطلوب لتمكين مدخل العميل</span><span class="sxs-lookup"><span data-stu-id="62413-116">Required setup to enable the Customer portal</span></span>

<span data-ttu-id="62413-117">بعد أن تتأكد من امتلاك التراخيص المطلوبة، يمكنك إعداد الكتابة المزدوجة كما ورد في [إرشادات المزامنة الأولية للكتابة المزدوجة](../../fin-ops-core/dev-itpro/data-entities/dual-write/initial-sync.md).</span><span class="sxs-lookup"><span data-stu-id="62413-117">After you've made sure that you have the required licenses, you can set up dual-write as described in the [dual-write initial synchronization instructions](../../fin-ops-core/dev-itpro/data-entities/dual-write/initial-sync.md).</span></span>

<span data-ttu-id="62413-118">تأكد من تمكين تعيينات الجداول التالية في الكتابة المزدوجة:</span><span class="sxs-lookup"><span data-stu-id="62413-118">Be sure to enable the following table mappings in dual-write:</span></span>

- <span data-ttu-id="62413-119">رأس أمر المبيعات</span><span class="sxs-lookup"><span data-stu-id="62413-119">Sales Order Header</span></span>
- <span data-ttu-id="62413-120">تفاصيل أمر المبيعات</span><span class="sxs-lookup"><span data-stu-id="62413-120">Sales Order Details</span></span>
- <span data-ttu-id="62413-121">الحسابات</span><span class="sxs-lookup"><span data-stu-id="62413-121">Accounts</span></span>
- <span data-ttu-id="62413-122">جهات الاتصال</span><span class="sxs-lookup"><span data-stu-id="62413-122">Contacts</span></span>
- <span data-ttu-id="62413-123">المنتجات</span><span class="sxs-lookup"><span data-stu-id="62413-123">Products</span></span>

<span data-ttu-id="62413-124">بعد اكتمال هذا الإعداد، يمكنك تزويد قالب مدخل العميل.</span><span class="sxs-lookup"><span data-stu-id="62413-124">After this setup is completed, you can provision the Customer portal template.</span></span>

## <a name="provision-the-customer-portal"></a><span data-ttu-id="62413-125">تزويد مدخل العميل</span><span class="sxs-lookup"><span data-stu-id="62413-125">Provision the Customer portal</span></span>

<span data-ttu-id="62413-126">قبل البدء، تأكد من إكمال [الإعداد المطلوب](#required-setup).</span><span class="sxs-lookup"><span data-stu-id="62413-126">Before you begin, make sure that you've already completed the [required setup](#required-setup).</span></span> <span data-ttu-id="62413-127">ثم اتبع الخطوات التالية لتزويد مدخل العميل.</span><span class="sxs-lookup"><span data-stu-id="62413-127">Then follow these steps to provision the Customer portal.</span></span>

1. <span data-ttu-id="62413-128">انتقل إلى [make.powerapps.com](https://make.powerapps.com/).</span><span class="sxs-lookup"><span data-stu-id="62413-128">Go to [make.powerapps.com](https://make.powerapps.com/).</span></span>
2. <span data-ttu-id="62413-129">تأكد من استخدام البيئة حيث قمت بتمكين الكتابة المزدوجة.</span><span class="sxs-lookup"><span data-stu-id="62413-129">Make sure that you're using the environment where you enabled dual-write.</span></span>
3. <span data-ttu-id="62413-130">من علامة التبويب **إنشاء**، قم بالتمرير لأسفل إلى القسم **بدء من القالب**، وحدد القالب المسمى **مدخل العميل**.</span><span class="sxs-lookup"><span data-stu-id="62413-130">On the **Create** tab, scroll down to the **Start from template** section, and select the template that is named **Customer Portal**.</span></span>
4. <span data-ttu-id="62413-131">اتبع الإرشادات التي تظهر على الشاشة.</span><span class="sxs-lookup"><span data-stu-id="62413-131">Follow the on-screen instructions.</span></span>

<span data-ttu-id="62413-132">بعد اكتمال التزويد، يمكنك الوصول إلى مدخل العميل في قسم **تطبيقاتك** في **الصفحة الرئيسية**.</span><span class="sxs-lookup"><span data-stu-id="62413-132">After provisioning is completed, you can access the Customer portal in the **Your apps** section of the **Home** page.</span></span>

> [!NOTE]
> <span data-ttu-id="62413-133">إذا لم يكن حل الكتابة المزدوجة مثبتًا في البيئة التي تعمل فيها، فستتلقى رسالة خطأ، ولن يتم تزويد مدخل العميل.</span><span class="sxs-lookup"><span data-stu-id="62413-133">If the dual-write solution isn't installed in the environment that you're working in, you will receive an error message, and the Customer portal won't be provisioned.</span></span>

## <a name="update-the-customer-portal"></a><span data-ttu-id="62413-134">تحديث مدخل العميل</span><span class="sxs-lookup"><span data-stu-id="62413-134">Update the Customer portal</span></span>

<span data-ttu-id="62413-135">قد تُضاف وظائف إضافية إلى مدخل العميل لاحقًا.</span><span class="sxs-lookup"><span data-stu-id="62413-135">More functionality might be added to the Customer portal later.</span></span> <span data-ttu-id="62413-136">ستظهر تلقائيًا في بيئتك التغييرات التي تجريها Microsoft على مكون الحل الأساسية.</span><span class="sxs-lookup"><span data-stu-id="62413-136">Any changes that Microsoft makes to the underlying solution components will automatically appear in your environment.</span></span> <span data-ttu-id="62413-137">ومع ذلك، فإن موقع الويب الذي تم تزويده في بيئتك لن يعكس التغييرات التي يتم إدخالها على بيانات التكوين.</span><span class="sxs-lookup"><span data-stu-id="62413-137">However, the website that is provisioned in your environment won't automatically reflect changes that are made to the configuration data.</span></span> <span data-ttu-id="62413-138">سيتعين عليك تطبيق هذه التغييرات يدويًا عن طريق الحصول على التعليمات البرمجية من القالب الجديد ودمجه مع موقع ويب الذي تم تزويده.</span><span class="sxs-lookup"><span data-stu-id="62413-138">You will have to manually apply those changes by getting the code from the new template and merging it with the provisioned website.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="62413-139">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="62413-139">Additional resources</span></span>

<span data-ttu-id="62413-140">لمعرفة كيفية إعداد مدخل العميل وتخصيصه، يجب البدء بمراجعة الوثائق التالية للتقنيات الأساسية:</span><span class="sxs-lookup"><span data-stu-id="62413-140">To learn how you can set up and customize the Customer portal, you should start by reviewing the following documentation for the underlying technologies:</span></span>

- [<span data-ttu-id="62413-141">وثائق مداخل Power Apps</span><span class="sxs-lookup"><span data-stu-id="62413-141">Power Apps portals documentation</span></span>](https://docs.microsoft.com/powerapps/maker/portals/overview)
- [<span data-ttu-id="62413-142">وثائق الكتابة المزدوجة</span><span class="sxs-lookup"><span data-stu-id="62413-142">Dual-write documentation</span></span>](../../fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-home-page.md)

<span data-ttu-id="62413-143">لإدارة المداخل بطريقة فعالة، يجب فهم مداخل Power Apps ودورة حياة Microsoft Dataverse.</span><span class="sxs-lookup"><span data-stu-id="62413-143">To effectively manage your portals, you must understand the Power Apps portals and Microsoft Dataverse lifecycle.</span></span> <span data-ttu-id="62413-144">لمزيد من المعلومات، راجع الموارد التالية:</span><span class="sxs-lookup"><span data-stu-id="62413-144">For more information, see the following resources:</span></span>

- [<span data-ttu-id="62413-145">حول دورة حياة المدخل</span><span class="sxs-lookup"><span data-stu-id="62413-145">About portal lifecycle</span></span>](https://docs.microsoft.com/powerapps/maker/portals/admin/portal-lifecycle)
- [<span data-ttu-id="62413-146">ترقية مدخل</span><span class="sxs-lookup"><span data-stu-id="62413-146">Upgrade a portal</span></span>](https://docs.microsoft.com/powerapps/maker/portals/admin/upgrade-portal)
- [<span data-ttu-id="62413-147">ترحيل تكوين المدخل</span><span class="sxs-lookup"><span data-stu-id="62413-147">Migrate portal configuration</span></span>](https://docs.microsoft.com/powerapps/maker/portals/admin/migrate-portal-configuration)
- [<span data-ttu-id="62413-148">إدارة دورة حياة الحل: تطبيقات Dynamics 365 for Customer Engagement</span><span class="sxs-lookup"><span data-stu-id="62413-148">Solution Lifecycle Management: Dynamics 365 for Customer Engagement apps</span></span>](https://www.microsoft.com/download/details.aspx?id=57777)
