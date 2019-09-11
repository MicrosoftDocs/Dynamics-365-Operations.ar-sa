---
title: إدارة قوالب البريد الإلكتروني
description: يشرح هذا الموضوع كيفية إدارة قوالب البريد الإلكتروني.
author: andreabichsel
manager: AnnBe
ms.date: 08/02/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: HRMApplicationWordBookmark, HRMApplicationEmailTemplate
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3ecfa720dfa9b3ed6ee15ec68498d2a46612a9ae
ms.sourcegitcommit: a368682f9cf3897347d155f1a2d4b33e555cc2c4
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/08/2019
ms.locfileid: "1867477"
---
# <a name="manage-email-templates"></a><span data-ttu-id="7da9c-103">إدارة قوالب البريد الإلكتروني</span><span class="sxs-lookup"><span data-stu-id="7da9c-103">Manage email templates</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="7da9c-104">يمكنك نقل المعلومات من قاعدة بيانات مؤسستك إلى الإشارات المرجعية في مستند جديد واستخدامها في قوالب تساعدك على التواصل بكفاءة مع مقدمي الطلبات والمرشحين.</span><span class="sxs-lookup"><span data-stu-id="7da9c-104">You can transfer information from your organization’s database to the bookmarks in a new document and use it in templates that help you communicate efficiently with applicants and candidates.</span></span> <span data-ttu-id="7da9c-105">لإجراء ذلك، يجب إنشاء قالب يتضمن نصًا قياسيًا وبعض الإشارات المرجعية حيث يجب إدراج بيانات النظام.</span><span class="sxs-lookup"><span data-stu-id="7da9c-105">To do this, you create a template that contains standard text and some bookmarks where the system data should be inserted.</span></span> <span data-ttu-id="7da9c-106">على سبيل المثال، يمكنك إدراج معلومات العنوان والاتصال الخاصة بمقدم الطلب في مستند Microsoft Word يمكنك استخدامه عند التواصل مع مقدم الطلب هذا.</span><span class="sxs-lookup"><span data-stu-id="7da9c-106">For example, you can insert address and contact information for an applicant into a Microsoft Word document that you can use when communicating with that applicant.</span></span> <span data-ttu-id="7da9c-107">شركة بيانات العرض التوضيحي التي تم استخدامها لإنشاء هذا الإجراء هي USMF.</span><span class="sxs-lookup"><span data-stu-id="7da9c-107">The demo data company used to create this procedure is USMF.</span></span>


## <a name="select-which-bookmarks-to-use-in-your-email-templates"></a><span data-ttu-id="7da9c-108">تحديد الإشارات المرجعية التي يجب استخدامها في قوالب البريد الإلكتروني</span><span class="sxs-lookup"><span data-stu-id="7da9c-108">Select which bookmarks to use in your email templates</span></span>
1. <span data-ttu-id="7da9c-109">في جزء التنقل، انتقل إلى **الوحدات النمطية > الموارد البشرية > التوظيف > الاتصال > العلامات المرجعية لاستمارات التقديم‬**.</span><span class="sxs-lookup"><span data-stu-id="7da9c-109">In the navigation pane, go to **Modules > Human Resources > Recruitment > Communication > Application bookmarks**.</span></span>
2. <span data-ttu-id="7da9c-110">في القائمة، ابحث عن إجراء المراسلات المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="7da9c-110">In the list, find and select the desired correspondence action.</span></span>
3. <span data-ttu-id="7da9c-111">حدد **تحرير**.</span><span class="sxs-lookup"><span data-stu-id="7da9c-111">Select **Edit**.</span></span>
4. <span data-ttu-id="7da9c-112">حدد الحقول التي تريد أن تكون قادرًا على استخدامها في قالب بريد إلكتروني لإجراء المراسلات المحدد ونقلها إلى حقول الإشارة المرجعية.</span><span class="sxs-lookup"><span data-stu-id="7da9c-112">Select the fields you would like to be able to use in an email template for the selected Correspondence action and move them to the Bookmark fields.</span></span>  
5. <span data-ttu-id="7da9c-113">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="7da9c-113">Close the page.</span></span>

## <a name="create-an-email-template"></a><span data-ttu-id="7da9c-114">إنشاء قالب بريد إلكتروني</span><span class="sxs-lookup"><span data-stu-id="7da9c-114">Create an email template</span></span>
1. <span data-ttu-id="7da9c-115">في جزء التنقل، انتقل إلى **الوحدات النمطية > الموارد البشرية > التوظيف > الاتصال > قوالب البريد الإلكتروني لاستمارات التقديم‬‬**.</span><span class="sxs-lookup"><span data-stu-id="7da9c-115">In the navigation pane, go to **Modules > Human resources > Recruitment > Communication > Application e-mail templates**.</span></span>
2. <span data-ttu-id="7da9c-116">حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="7da9c-116">Select **New**.</span></span>
3. <span data-ttu-id="7da9c-117">في الحقل **إجراء المراسلات**، حدد **مقابلة‬**.</span><span class="sxs-lookup"><span data-stu-id="7da9c-117">In the **Correspondence action** field, select **Interview**.</span></span> <span data-ttu-id="7da9c-118">حدد إجراء المراسلات الذي يحتوي على الإشارات المرجعية التي يجب استخدامها لهذا النوع من المراسلات الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="7da9c-118">Select the correspondence action that contains the bookmarks to use for this type of email communication.</span></span>  
4. <span data-ttu-id="7da9c-119">في الحقل **قالب بريد إلكتروني**، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="7da9c-119">In the **E-mail template** field, type a value.</span></span>
5. <span data-ttu-id="7da9c-120">في الحقل **الموضوع**، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="7da9c-120">In the **Subject** field, type a value.</span></span>
6. <span data-ttu-id="7da9c-121">في الحقل **النص**، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="7da9c-121">In the **Text** field, type a value.</span></span>
7. <span data-ttu-id="7da9c-122">في القائمة، ابحث عن حقل الإشارة المرجعية المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="7da9c-122">In the list, find and select the desired bookmark field.</span></span>
8. <span data-ttu-id="7da9c-123">تابع كتابة رسالة البريد الإلكتروني، مع إدراج حقول الإشارة المرجعية حيث تحتاج إليها.</span><span class="sxs-lookup"><span data-stu-id="7da9c-123">Continue typing your email message, inserting the bookmark fields where you need them.</span></span>
9. <span data-ttu-id="7da9c-124">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="7da9c-124">Select **Save**.</span></span>

