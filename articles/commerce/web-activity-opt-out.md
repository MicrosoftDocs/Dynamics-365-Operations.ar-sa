---
title: إلغاء الاشتراك من مجموعة أحداث نشاط الويب
description: يشرح هذا الموضوع كيفية السماح لزوار موقع ويب الخاص بك بإلغاء الاشتراك من مجموعة أحداث نشاط الويب في Microsoft Dynamics 365 Commerce.
author: aamiral
manager: AnnBe
ms.date: 05/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Retail, eCommerce
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 4b0e48307527a8fea729d8dfdcdbc6337be0faf1
ms.sourcegitcommit: 8058db089b8768076ff1250be77d42a6e2b3f570
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/15/2020
ms.locfileid: "3378982"
---
# <a name="opt-out-of-web-activity-event-collection"></a><span data-ttu-id="c9e31-103">إلغاء الاشتراك من مجموعة أحداث نشاط الويب</span><span class="sxs-lookup"><span data-stu-id="c9e31-103">Opt out of web activity event collection</span></span>
[!include [banner](includes/banner.md)]

<span data-ttu-id="c9e31-104">يشرح هذا الموضوع كيفية السماح للعملاء بإلغاء الاشتراك من مجموعة أحداث نشاط الويب في Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="c9e31-104">This topic explains how you can let customers opt out of web activity event collection in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="c9e31-105">نظرة عامة</span><span class="sxs-lookup"><span data-stu-id="c9e31-105">Overview</span></span>

<span data-ttu-id="c9e31-106">يتيح Dynamics 365 Commerce لمسؤولي المواقع تحليل نشاط الويب لمستخدمي مواقع التجارة الإلكترونية الخاصة بهم.</span><span class="sxs-lookup"><span data-stu-id="c9e31-106">Dynamics 365 Commerce lets site administrators analyze the web activity of users of their e-commerce sites.</span></span> <span data-ttu-id="c9e31-107">وبهذه الطريقة، يمكنهم فهم كيف يتم استخدام مواقعهم بشكل أفضل، كما يمكنهم تحسين المواقع لتوفير تجربة مستخدم محسنة وتلبية أهداف الأعمال.</span><span class="sxs-lookup"><span data-stu-id="c9e31-107">In that way, they can better understand how their sites are used, and they can optimize the sites to provide an improved user experience and meet business objectives.</span></span>


## <a name="ways-for-administrators-to-implement-an-opt-out-experience"></a><span data-ttu-id="c9e31-108">طرق للمسؤولين لتنفيذ تجربة إلغاء الاشتراك</span><span class="sxs-lookup"><span data-stu-id="c9e31-108">Ways for administrators to implement an opt-out experience</span></span>

<span data-ttu-id="c9e31-109">يتوفر للمسؤولين ثلاث طرق لتنفيذ تجربة إلغاء الاشتراك.</span><span class="sxs-lookup"><span data-stu-id="c9e31-109">Administrators have three ways to implement an opt-out experience.</span></span>

### <a name="opt-out-on-behalf-of-users"></a><span data-ttu-id="c9e31-110">إلغاء الاشتراك نيابةً عن المستخدمين</span><span class="sxs-lookup"><span data-stu-id="c9e31-110">Opt out on behalf of users</span></span>

<span data-ttu-id="c9e31-111">في إدارة الحسابات في Commerce headquarters (HQ)، يمكن للمسؤولين إلغاء الاشتراك بالنيابة عن المستخدمين.</span><span class="sxs-lookup"><span data-stu-id="c9e31-111">In Account management in Commerce headquarters (HQ), administrators can opt out on behalf of users.</span></span>

1. <span data-ttu-id="c9e31-112">في عميل HQ ، في صفحة **كافة العملاء**، ابحث عن عميل وحدده.</span><span class="sxs-lookup"><span data-stu-id="c9e31-112">In the HQ client, on the **All customers** page, search for and select a customer.</span></span>
1. <span data-ttu-id="c9e31-113">من الصفحة تفاصيل العميل، في علامة التبويب السريعة **البيع بالتجزئة**، في قسم **الخصوصية**، قم بتعيين خيار **عدم تعقب نشاط الويب** إلى **نعم**.</span><span class="sxs-lookup"><span data-stu-id="c9e31-113">On the customer details page, on the **Retail** FastTab, in the **Privacy** section, set the **Do not track web activity** option to **Yes**.</span></span>

    ![إعدادات الخصوصية](media/Disablepersonalizationpart2.png)

1. <span data-ttu-id="c9e31-115">حدد **حفظ** ثم قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="c9e31-115">Select **Save**, and then close the page.</span></span>

### <a name="module-based-opt-out-experience"></a><span data-ttu-id="c9e31-116">تجربه إلغاء الاشتراك المستند إلى الوحدة النمطية</span><span class="sxs-lookup"><span data-stu-id="c9e31-116">Module-based opt-out experience</span></span>

<span data-ttu-id="c9e31-117">يمكن للمسؤولين السماح للمستخدمين المصادق عليهم بإلغاء الاشتراك من مجموعة أحداث نشاط الويب بأنفسهم.</span><span class="sxs-lookup"><span data-stu-id="c9e31-117">Administrators can let authenticated users opt out of web activity event collection by themselves.</span></span> <span data-ttu-id="c9e31-118">لتوفير تجربه إلغاء الاشتراك هذه ، أضف الوحدة النمطية للغاء اشتراك المستخدم إلى صفحات ملف تعريف حساب العميل.</span><span class="sxs-lookup"><span data-stu-id="c9e31-118">To provide this opt-out experience, add the user opt-out module to customer account profile pages.</span></span>

### <a name="custom-extensions"></a><span data-ttu-id="c9e31-119">الملحقات المخصصة</span><span class="sxs-lookup"><span data-stu-id="c9e31-119">Custom extensions</span></span>

<span data-ttu-id="c9e31-120">يمكن للمسؤولين إنشاء الملحقات الخاصة بهم لإدارة تجربة إلغاء الاشتراك للمستخدمين.</span><span class="sxs-lookup"><span data-stu-id="c9e31-120">Administrators can create their own extensions to manage the opt-out experience for users.</span></span> <span data-ttu-id="c9e31-121">لمزيد من المعلومات، راجع [استدعاء واجهات برمجة تطبيقات Retail Server](e-commerce-extensibility/call-retail-server-apis.md) و[توسعة القنوات على الإنترنت](e-commerce-extensibility/overview.md).</span><span class="sxs-lookup"><span data-stu-id="c9e31-121">For more information, see [Call Retail Server APIs](e-commerce-extensibility/call-retail-server-apis.md) and [Online channel extensibility](e-commerce-extensibility/overview.md).</span></span>
