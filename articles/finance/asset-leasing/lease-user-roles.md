---
title: تعيين أدوار مستخدم عقد الإيجار
description: يصف هذا الموضوع أدوار الأمان المستخدمة في تأجير الأصول. كما يوضح كيفية تعيين مستخدمين لهذه الأدوار.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 09d80e9629b60144665441989d9d63d7f6be3c60
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/15/2021
ms.locfileid: "5207269"
---
# <a name="assign-lease-user-roles"></a><span data-ttu-id="63c6b-104">تعيين أدوار مستخدم عقد الإيجار</span><span class="sxs-lookup"><span data-stu-id="63c6b-104">Assign lease user roles</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="63c6b-105">يصف هذا الموضوع أدوار الأمان المستخدمة في تأجير الأصول.</span><span class="sxs-lookup"><span data-stu-id="63c6b-105">This topic describes the security roles that are used in Asset leasing.</span></span> <span data-ttu-id="63c6b-106">كما يوضح كيفية تعيين مستخدمين لهذه الأدوار.</span><span class="sxs-lookup"><span data-stu-id="63c6b-106">It also explains how to assign users to those roles.</span></span>

<span data-ttu-id="63c6b-107">تتميز أدوار المستخدمين الثلاثة بالوصول في تأجير الأصول.</span><span class="sxs-lookup"><span data-stu-id="63c6b-107">Three user roles differentiate access in Asset leasing.</span></span> <span data-ttu-id="63c6b-108">يعد أحد الأدوار مناسبًا للحفاظ عقود الإيجار، وهو الأنسب لعرض عقود الإيجار، ويكون الدور مناسبًا لتنفيذ مهام موظف الإيجار.</span><span class="sxs-lookup"><span data-stu-id="63c6b-108">One role is appropriate for maintaining leases, one is appropriate for viewing leases, and one is appropriate for performing a lease clerk's duties.</span></span> <span data-ttu-id="63c6b-109">ولكل دور أذونات محددة لكافة صفحات عقود الإيجار، ويتيح كل من المستخدمين عرض عقود الإيجار أو إنشاءها أو تحريرها أو حذفها وفقًا لمهام الوظائف الخاصة بهم.</span><span class="sxs-lookup"><span data-stu-id="63c6b-109">Each role has specific permissions for all lease pages, and each lets users view, create, edit, or delete leases, according to their job duties.</span></span>

| <span data-ttu-id="63c6b-110">دور</span><span class="sxs-lookup"><span data-stu-id="63c6b-110">Role</span></span>           | <span data-ttu-id="63c6b-111">الوصف</span><span class="sxs-lookup"><span data-stu-id="63c6b-111">Description</span></span> |
|----------------|-------------|
| <span data-ttu-id="63c6b-112">المحافظة على عقد الإيجار</span><span class="sxs-lookup"><span data-stu-id="63c6b-112">Maintain Lease</span></span> | <span data-ttu-id="63c6b-113">يمكن للمستخدمين في هذا الدور إضافة عقود الإيجار وتحريرها وحذفها وعرضها.</span><span class="sxs-lookup"><span data-stu-id="63c6b-113">Users in this role can add, edit, delete, and view leases.</span></span> <span data-ttu-id="63c6b-114">تم تصميم هذا الدور للمستخدمين اليوميين الذين تشتمل مهامهم على إنشاء إدخالات دفتر يومية شهري وترحيلها وإضافة عقود إيجار جديدة.</span><span class="sxs-lookup"><span data-stu-id="63c6b-114">This role is designed for daily users whose tasks include creating and posting monthly journal entries and adding new leases.</span></span> <span data-ttu-id="63c6b-115">يمنح هذا الدور حق الوصول إلى كافة وظائف تأجير الأصول.</span><span class="sxs-lookup"><span data-stu-id="63c6b-115">This role gives access to all Asset leasing functionality.</span></span> |
| <span data-ttu-id="63c6b-116">عرض عقد الإيجار</span><span class="sxs-lookup"><span data-stu-id="63c6b-116">View Lease</span></span>     | <span data-ttu-id="63c6b-117">يمكن للمستخدمين في هذا الدور عرض سجلات عقود الإيجار والجداول وتشغيل التقارير فقط.</span><span class="sxs-lookup"><span data-stu-id="63c6b-117">Users in this role can only view lease records, schedules, and run reports.</span></span> <span data-ttu-id="63c6b-118">ولا يمكنهم إنشاء عقود إيجار جديدة أو تحرير عقود إيجار موجودة أو إنشاء إدخالات دفاتر يومية ضد عقود الإيجار.</span><span class="sxs-lookup"><span data-stu-id="63c6b-118">They can't create new leases, edit existing leases, or create journal entries against leases.</span></span> <span data-ttu-id="63c6b-119">تم تصميم الدور للمستخدمين المضطرين إلى عرض عقود الإيجار وجداول عقود الإيجار والحركات التي تحدث في مقابل عقود الإيجار هذه فقط.</span><span class="sxs-lookup"><span data-stu-id="63c6b-119">The role is designed for users who just have to view leases, lease schedules, and the transactions that occur against those leases.</span></span> |
| <span data-ttu-id="63c6b-120">موظف الإيجار</span><span class="sxs-lookup"><span data-stu-id="63c6b-120">Lease Clerk</span></span>    | <span data-ttu-id="63c6b-121">يمكن للمستخدمين في هذا الدور إنشاء عقود إيجار جديدة فقط.</span><span class="sxs-lookup"><span data-stu-id="63c6b-121">Users in this role can only create new leases.</span></span> <span data-ttu-id="63c6b-122">ولا يمكنهم تحرير عقود الإيجار الحالية أو حذفها أو عرض جداول عقد الإيجار أو ترحيل إدخالات دفتر يومية للتأجير.</span><span class="sxs-lookup"><span data-stu-id="63c6b-122">They can't edit or delete existing leases, view lease schedules, or post leasing journal entries.</span></span> <span data-ttu-id="63c6b-123">تم تصميم هذا الدور للمستخدمين الذين يعملون في قدرة إدخال البيانات.</span><span class="sxs-lookup"><span data-stu-id="63c6b-123">This role is designed for users who work in a data entry capacity.</span></span> |

<span data-ttu-id="63c6b-124">اتبع الخطوات التالية لتعيين المستخدمين إلى الأدوار المستخدمة في تأجير الأصول.</span><span class="sxs-lookup"><span data-stu-id="63c6b-124">Follow these steps to assign users to the roles that are used in Asset leasing.</span></span>

1. <span data-ttu-id="63c6b-125">انتقل إلى **إدارة النظام \> الأمان \> تعيين مستخدمين للأدوار**.</span><span class="sxs-lookup"><span data-stu-id="63c6b-125">Go to **System administration \> Security \> Assign users to roles**.</span></span>
2. <span data-ttu-id="63c6b-126">حدد الدور **المحافظة على عقد الإيجار** أو **موظف الإيجار** أو **عرض عقد الإيجار**، ثم حدد **تعيين/استبعاد المستخدمين يدويًا**.</span><span class="sxs-lookup"><span data-stu-id="63c6b-126">Select the **Maintain lease**, **Lease clerk**, or **View lease** role, and then select **Manually assign/exclude users**.</span></span>
3. <span data-ttu-id="63c6b-127">حدد المستخدم المراد تعيينه للدور، ثم حدد **تعيين إلى دور**.</span><span class="sxs-lookup"><span data-stu-id="63c6b-127">Select the user to assign to the role, and then select **Assign to role**.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]