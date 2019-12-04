---
title: تمكين تكامل Broadbean في Attract
description: يشرح هذا الموضوع كيفية تكوين Microsoft Dynamics 365 Talent - Attract لنشر الوظائف في لوحات وظائف خارجية مثل Broadbean.
author: andreabichsel
manager: AnnBe
ms.date: 07/08/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2019-07-08
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: 10b612711e81b2b368ed23fdd95ab6a66451f0ca
ms.sourcegitcommit: 9cc6a011bfdd1b0fe505760b6bf429eb6c65862a
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 11/25/2019
ms.locfileid: "2833198"
---
# <a name="enable-broadbean-integration-in-attract"></a><span data-ttu-id="7e206-103">تمكين تكامل Broadbean في Attract</span><span class="sxs-lookup"><span data-stu-id="7e206-103">Enable Broadbean integration in Attract</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="7e206-104">تريد عرض المناصب المفتوحة أمام عدد أكبر عدد ممكن من المرشحين المؤهلين.</span><span class="sxs-lookup"><span data-stu-id="7e206-104">You want to get your open positions in front of as many qualified candidates as possible.</span></span> <span data-ttu-id="7e206-105">تساعدك مواقع التوظيف مثل Broadbean في تحقيق هذا الهدف.</span><span class="sxs-lookup"><span data-stu-id="7e206-105">Recruiting sites such as Broadbean help you accomplish this goal.</span></span> <span data-ttu-id="7e206-106">يسمح لك الآن Microsoft Dynamics 365 Talent: Attract بنشر الوظائف في Broadbean، وتعمل Microsoft بشكل مستمر على تقديم عروض جديدة في هذا المجال.</span><span class="sxs-lookup"><span data-stu-id="7e206-106">Microsoft Dynamics 365 Talent: Attract now lets you post jobs to Broadbean, and Microsoft is constantly providing new offerings in this area.</span></span>

> [!NOTE]
> - <span data-ttu-id="7e206-107">لنشر الوظائف في مواقع خارجية، يجب استخدام [المكون الإضافي "التوظيف الشامل"](https://docs.microsoft.com/dynamics365/unified-operations/talent/attract-comprehensive-hiring).</span><span class="sxs-lookup"><span data-stu-id="7e206-107">To post jobs to external sites, you must have the [Comprehensive hiring add-on](https://docs.microsoft.com/dynamics365/unified-operations/talent/attract-comprehensive-hiring).</span></span>
> - <span data-ttu-id="7e206-108">لترحيل الوظائف إلى Broadbean من خلال Attract، يجب أن يكون لديك اشتراك Broadbean.</span><span class="sxs-lookup"><span data-stu-id="7e206-108">To post jobs to Broadbean through Attract, you must have a Broadbean subscription.</span></span>
> - <span data-ttu-id="7e206-109">هذه الميزة قيد المعاينة حاليًا.</span><span class="sxs-lookup"><span data-stu-id="7e206-109">This feature is currently in preview.</span></span> <span data-ttu-id="7e206-110">إذا أردت تجربتها، فيجب [تشغيلها في إعدادات إدارة Attract](https://docs.microsoft.com/dynamics365/unified-operations/talent/access-preview-feature).</span><span class="sxs-lookup"><span data-stu-id="7e206-110">If you want to try it, you must [turn it on in the Attract admin settings](https://docs.microsoft.com/dynamics365/unified-operations/talent/access-preview-feature).</span></span>

## <a name="configure-broadbean-integration"></a><span data-ttu-id="7e206-111">تكوين تكامل Broadbean</span><span class="sxs-lookup"><span data-stu-id="7e206-111">Configure Broadbean integration</span></span>

1. <span data-ttu-id="7e206-112">سجل دخولك إلى Attract كمسؤول.</span><span class="sxs-lookup"><span data-stu-id="7e206-112">Sign in to Attract as an admin.</span></span>

2. <span data-ttu-id="7e206-113">حدد زر **الإعدادات** (رمز الترس) في الزاوية العلوية اليسرى من الصفحة، ثم حدد **مركز الإدارة**.</span><span class="sxs-lookup"><span data-stu-id="7e206-113">Select the **Settings** button (the gear symbol) in the upper-right corner of the page, and then select **Admin center**.</span></span>

3. <span data-ttu-id="7e206-114">اتصل بموقع Broadbean، وأدخل معلوماتك في حقول **اسم المستخدم** و**معرف العميل** و**رمز التشفير**.</span><span class="sxs-lookup"><span data-stu-id="7e206-114">Contact Broadbean, and enter your information in the **Username**, **Client ID**, and **Encryption Token** fields.</span></span>

4. <span data-ttu-id="7e206-115">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="7e206-115">Select **Save**.</span></span>

> [!WARNING]
> <span data-ttu-id="7e206-116">تعتبر بيانات اعتمادك في Broadbean سرية وحساسة لحالة الأحرف.</span><span class="sxs-lookup"><span data-stu-id="7e206-116">Your Broadbean credentials are sensitive and confidential.</span></span> <span data-ttu-id="7e206-117">وبالتالي، يجب تخزينها ومشاركتها بطريقة مسؤولة.</span><span class="sxs-lookup"><span data-stu-id="7e206-117">Therefore, store and share them responsibly.</span></span> <span data-ttu-id="7e206-118">بإمكان أي شخص يؤدي دور المسؤول في Attract عرض بيانات الاعتماد هذه.</span><span class="sxs-lookup"><span data-stu-id="7e206-118">Anyone who has an Administrator role in Attract can view these credentials.</span></span>

> [!NOTE]
> <span data-ttu-id="7e206-119">لا تشارك Microsoft كما لا يشارك Attract في إنشاء هذه القيم والمحافظة عليها.</span><span class="sxs-lookup"><span data-stu-id="7e206-119">Microsoft and Attract aren't involved in creating and maintaining these values.</span></span> <span data-ttu-id="7e206-120">تقع على عاتقك مسؤولية تحديثها بشكل مستمر في Attract والعمل مع Broadbean على حل أي مشكلة تتعلق ببيانات اعتمادك.</span><span class="sxs-lookup"><span data-stu-id="7e206-120">It's your responsibility to keep them up to date in Attract and to work with Broadbean to resolve any issues that involve your credentials.</span></span>
